#import "OEN64SystemController.h"
#import "OEN64SystemResponder.h"
#import "OEN64SystemResponderClient.h"

#import <OpenEmuSystem/OpenEmuSystem.h>

@implementation OEN64SystemController

- (NSString *)headerLookupForFile:(__kindof OEFile *)file
{
    // Read the full 64 byte header
    NSData *dataBuffer = [file readDataInRange:NSMakeRange(0, 64)];

    unsigned char temp;
    unsigned char *rom = (unsigned char *)[dataBuffer bytes];
    NSUInteger romSize = [dataBuffer length];
    
    // Read the first 4 bytes of the header to get the 'magic word' in hex
    NSMutableString *hexString = [[NSMutableString alloc] initWithCapacity:4];
    for(NSUInteger i = 0; i < 4;)
    {
        [hexString appendFormat:@"%02X", rom[i]];
        i++;
    }
    
    // Detect rom formats using 'magic word' hex and swap byte order to [ABCD] if neccessary
    // .z64 rom is N64 native (big endian) with header 0x80371240 [ABCD], no need to swap
    
    // Byteswapped .v64 rom with header 0x37804012 [BADC]
    if([hexString isEqualToString:@"37804012"])
    {
        for(int i = 0; i < romSize; i+=2)
        {
            temp=rom[i];
            rom[i]=rom[i+1];
            rom[i+1]=temp;
        }
    }
    // Little endian .n64 rom with header 0x40123780 [DCBA]
    else if([hexString isEqualToString:@"40123780"])
    {
        for(NSUInteger i = 0; i < romSize; i+=4)
        {
            temp=rom[i];
            rom[i]=rom[i+3];
            rom[i+3]=temp;
            temp=rom[i+1];
            rom[i+1]=rom[i+2];
            rom[i+2]=temp;
        }
    }
    // Wordswapped .n64 rom with header 0x12408037 [CDAB]
    else if([hexString isEqualToString:@"12408037"])
    {
        for(NSUInteger i = 0; i < romSize; i+=4)
        {
            temp=rom[i];
            rom[i]=rom[i+2];
            rom[i+2]=temp;
            temp=rom[i+1];
            rom[i+1]=rom[i+3];
            rom[i+3]=temp;
        }
    }

    // Final rom header in hex after any swapping that may have occured
    NSData *romBuffer = [NSData dataWithBytes:rom length:romSize];
    
    // Format the hexadecimal representation and return
    NSString *buffer = [[romBuffer description] uppercaseString];
    NSString *hex = [[buffer componentsSeparatedByCharactersInSet:[[NSCharacterSet alphanumericCharacterSet] invertedSet]] componentsJoinedByString:@""];
    
    return hex;
}