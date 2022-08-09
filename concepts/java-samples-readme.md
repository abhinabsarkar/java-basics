# Basic sample apps

## Spring Boot app
* [Building an Application with Spring Boot - Hello World](https://spring.io/guides/gs/spring-boot/)
* [Spring Boot Hello World - Create simple controller and jsp view](https://www.javainuse.com/spring/SpringBoot_HelloWorld)

```bash
# Hello World Spring Boot endpoint
http://localhost:8080/
# Spring Boot app with controller and jsp view
http://localhost:8080/welcome.html
```

* [Spring Boot - Session Management Using Redis](https://www.javainuse.com/spring/springboot_session_redis)
```bash
# Spring Boot Session Application endpoint
http://localhost:8080/
```

* Spring Boot - Session Management using Redis - Docker container
    * To do - useful links
        * https://spring.io/blog/2018/11/08/spring-boot-in-a-container
        * https://spring.io/guides/gs/spring-boot-docker/
        * https://spring.io/guides/gs/spring-boot/
        * https://stackoverflow.com/questions/31324981/how-to-access-host-port-from-docker-container
        * https://initialcommit.com/blog/run-jar-file-command-line
        * [Manage Kubernetes Secrets with Azure Key Vault](https://nileshgule.medium.com/how-to-manage-kubernetes-secrets-with-azure-key-vault-211cb989b86b)
            * [Kubernetes Secrets Store CSI Driver](https://github.com/kubernetes-sigs/secrets-store-csi-driver) - allows Kubernetes to mount multiple secrets, keys, and certs stored in enterprise-grade external secrets stores into their pods as a volume. Once the Volume is attached, the data in it is mounted into the container's file system.
            * [Azure Key Vault Provider for Secrets Store CSI Driver in an AKS cluster](https://docs.microsoft.com/en-us/azure/aks/csi-secrets-store-driver)
                * [Why mounting secrets as volume is secure in k8s?](https://stackoverflow.com/questions/55620043/is-there-any-security-advantage-to-mounting-secrets-as-a-file-instead-of-passing)
                * [Creating Kubernetes Secrets from Azure Key Vault with the CSI Driver](https://samcogan.com/creating-kubernetes-secrets-from-azure-key-vault-with-the-csi-driver/) - The Azure Key Vault CIS Driver is an extension for AKS that allows you to take secrets from Azure Key Vault and mount them as volumes in your pods. Your applications can then read the secret data from a volume mount inside the pod. This is great, but again it means you need to change your application to read from that volume.
                * [Azure Key Vault secrets provider extension for Arc enabled Kubernetes clusters](https://techcommunity.microsoft.com/t5/azure-arc-blog/in-preview-azure-key-vault-secrets-provider-extension-for-arc/ba-p/3002160)                
        * Spring Boot with Azure Redis Cache
            * [Spring Boot - Session management using Azure Redis Cache](https://docs.microsoft.com/en-us/azure/developer/java/spring-framework/configure-spring-boot-initializer-java-app-with-redis-cache)
            * [Spring Boot - Store HTTP session data in Redis](https://docs.microsoft.com/en-us/learn/modules/accelerate-scale-spring-boot-application-azure-cache-redis/6-exercise-store-session-data)

