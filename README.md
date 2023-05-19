# WAFF-B
## How we, @vidocsecurity, bypass 401 and 403 - practical tips for fellow #bugbounty hunters <thread>.
  
  
![1](https://github.com/nazmul-ethi/Bypass-401-and-403/assets/130249045/477fb003-1d2d-4dd7-ad3e-4070b0728451)

  
* Try fuzzing HTTP method/user agents, you would be surprised how many times simply changing User-Agent to e.g. mobile specific client worked.
  
![2](https://github.com/nazmul-ethi/Bypass-401-and-403/assets/130249045/3f30383e-ec1c-4775-a4d4-7d9a41b66453)
  
* Play with forward/referer type of headers and their values. Try different variants, fuzz common custom headers that follow the pattern with different formats of localhost/custom IP address.

  ![3](https://github.com/nazmul-ethi/Bypass-401-and-403/assets/130249045/bfe6ddce-13b0-41e8-be2b-c1cb4701fbd8)

  
* Try path fuzzing with creative string literals, downgrade HTTP version.

  ![4](https://github.com/nazmul-ethi/Bypass-401-and-403/assets/130249045/c2a4ca5a-44f2-48d1-a868-40d53e81dfff)


* Try to know as much as you can about the target technology. Good recon is a key, there are some technology-specific hacks, e.g. Spring in some older versions have specific workaround related to useSuffixPatternMatch. If set to true (default) /admin would also match /admin[.].*

  * When nothing works try less common techniques such as exploiting hop-to-hop headers - this is my favorite method, and I will write a separate thread about it. More about this technique can be found in our article: https://vidocsecurity.com/blog/401-and-403-bypass-how-to-do-it-right/
  
  * List of payloads for fuzzing is available in our Module Library - you can use them to automate work using Vidoc Research, method/headers fuzzing: https://app.vidocsecurity.com/public-library/65107c81-587e-4eff-b243-3afb05620fb8 and path fuzzing: https://app.vidocsecurity.com/public-library/5a838688-86db-4732-97af-cff51e663d8c
