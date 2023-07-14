# public-keys update #
## Requirement
+ Jenkins Server
+ Conjur Secrets plugin
+ Conjur Server
+ Conjur Policies
  * the host or user should have permission to only update the public-keys.
  * Here an Example
    ```
    - !permit
      resource: !variable conjur/authn-jwt/jenkins/public-keys
      privileges: [ update ]
      roles: !host jenkins/projects/jenkins
    ```

## Usage instructions
### Step by step guide
![image](https://github.com/ManithejaCyberark/public-keys-update/assets/109070761/1549416a-83c7-440f-8565-f95b3ccc1e6a)
<img width="900" alt="image" src="https://github.com/ManithejaCyberark/public-keys-update/assets/109070761/3aa4b0ac-83c5-4df2-9cf1-edbc0201e801">



Usage from Jenkins freestyle project
- To bind to Conjur secrets, use the option "Use secret text(s) or file(s)" in the "Build Environment" section of a Freestyle project
- <img width="1000" alt="image" src="https://github.com/ManithejaCyberark/public-keys-update/assets/109070761/ebcbe9e0-315b-4c9d-a24c-fa168eb6a840">


