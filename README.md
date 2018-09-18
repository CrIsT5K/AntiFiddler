Many have problems with fiddler, 
for example you need to send sensitive information to the web server,
or for example receive something important from the server and fiddler simply manipulates your request,
I will be making available a simple method to disrupt the fiddler, which can be useful against those who do not have much knowledge.
Code:
```csharp
 WebRequest wr = WebRequest.Create(URL); //Create WebRequest
            wr.Proxy = null; //This's the method to bypass missconfigured fiddler, fiddler need proxy to intercept/debug if proxy = null, he can't intercept
            string html = new System.IO.StreamReader(wr.GetResponse().GetResponseStream()).ReadToEnd(); //get Html
  ```
Thisn't full solution.
