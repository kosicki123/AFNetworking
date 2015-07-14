AFRestNetworking is a fork of AFNetworking. The main difference is that you can specify the format of query string on get requests.

Your query strings will be formatted like this:<br>
http://url/method/XXXXXX/30<br>
Instead of:<br>
http://url/method?token=XXXXXX&user=30<br>

E.g: When creating a RequestSerializer you'll use this method:
```objective-c
- (NSMutableURLRequest *)requestRestWithMethod:(NSString *)method
                                     URLString:(NSString *)URLString
                                    parameters:(id)parameters
                                         error:(NSError *__autoreleasing *)error;
```
Instead of:
```objective-c
- (NSURLRequest *)requestBySerializingRequest:(NSURLRequest *)request
                               withParameters:(id)parameters
                                        error:(NSError * __autoreleasing *)error;
```
