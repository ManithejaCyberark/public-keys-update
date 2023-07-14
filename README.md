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
