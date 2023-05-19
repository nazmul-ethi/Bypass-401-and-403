# WAFF-B
# How we, @vidocsecurity, bypass 401 and 403 - practical tips for fellow #bugbounty hunters <thread>.
  
  
![1](https://github.com/nazmul-ethi/Bypass-401-and-403/assets/130249045/477fb003-1d2d-4dd7-ad3e-4070b0728451)

  
* Try fuzzing HTTP method/user agents, you would be surprised how many times simply changing User-Agent to e.g. mobile specific client worked.
  
![2](https://github.com/nazmul-ethi/Bypass-401-and-403/assets/130249045/3f30383e-ec1c-4775-a4d4-7d9a41b66453)
  
* Play with forward/referer type of headers and their values. Try different variants, fuzz common custom headers that follow the pattern with different formats of localhost/custom IP address.

  ![3](https://github.com/nazmul-ethi/Bypass-401-and-403/assets/130249045/bfe6ddce-13b0-41e8-be2b-c1cb4701fbd8)

  
* Try path fuzzing with creative string literals, downgrade HTTP version.

  ![4](https://github.com/nazmul-ethi/Bypass-401-and-403/assets/130249045/c2a4ca5a-44f2-48d1-a868-40d53e81dfff)


