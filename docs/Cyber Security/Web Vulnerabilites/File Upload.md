
File upload feature is a common feature provided by many websites for sharing files, document and other files. This common feature pose significant security risks if not implemented correctly . 

basically it is related to unrestricted file upload . user file is not sufficiently validated  like name content type size
## Impact

**Depends upon two factor** 
- type of restrictions imposed on file once its uploaded on server
- which aspect of the file  the website fails to validate

## How do web servers handle requests for static files ?

- Identifying the file extension
- Checking whether the file is executable or non executable 
- if the files is non executable such as image then the server send the file content in http response
- if the file is executable such as php files the  server is configured to execute file of this type, -it will assign variables based on the headers and parameters in the HTTP request before running the script. The resulting output may then be sent to the client in an HTTP response.
- If the file type is executable, but the server **is not** configured to execute files of this type, it will generally respond with an error. However, in some cases, the contents of the file may still be served to the client as plain text. Such misconfigurations can occasionally be exploited to leak source code and other sensitive information. You can see an example of this in our information disclosure learning materials.


## Preventing file execution in user-accessible directories

Servers generally only run scripts whose MIME type they have been explicitly configured to execute. Otherwise, they may just return some kind of error message or, in some cases, serve the contents of the file as plain text instead

. A directory to which user-supplied files are uploaded will likely have much stricter controls than other locations on the filesystem that are assumed to be out of reach for end users. If you can find a way to upload a script to a different directory that's not supposed to contain user-supplied files, the server may execute your script after all.

![[Pasted image 20240603221208.png]]
## Web shell upload via path traversal

Now if the uploaded file is saved in a directory say filesUploaded and execution of file is disabled in this directory.

what we can do is in the file name we can use path traversal to save file to another directory where it is executable