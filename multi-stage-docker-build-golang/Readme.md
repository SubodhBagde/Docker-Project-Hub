# Multi Stage Docker Build using GoLang

</br >

### Explanation in Simple Points

</br >

1. **Why Choose Go (Golang)?**

</br >

   - Go is a statically-typed programming language.
   - It doesn't need a runtime environment like Python, Ruby, or JavaScript.
   - Go compiles directly to machine code.
   - The machine code runs directly on the operating system.

</br >

2. **Benefits of Using Go with Docker:**

</br >

   - Multi-stage Docker builds and distroless images are particularly useful.
   - These techniques drastically reduce the size of the Docker image.

</br >

By using Go with multi-stage Docker builds and distroless images, you get smaller, more efficient Docker images.

</br > 

## Follow the Steps to implement

</br >

1. Install Docker on your machine and check if it is Up and Running.

</br >

2.  Clone this repository and move to  dockerfile-without-multi-stage folder

</br >

```
git clone https://github.com/SubodhBagde/Docker-Project-Hub.git
cd dockerfile-without-multi-stage
```

</br >

3. Build your Docker Image 

</br >

```
docker build -t simplecalc .
```

</br >

4. Verify Docker Image is created

</br >

```
docker images
```

</br >

Output

</br >

```
REPOSITORY        TAG       IMAGE ID       CREATED          SIZE
subodhb57/sc      latest    7a503c453499   21 minutes ago   647MB
ubuntu            latest    35a88802559d   12 days ago      78.1MB
hello-world       latest    d2c94e258dcb   13 months ago    13.3kB
```

</br >

4. The size of image created for simple calc is 647MB. Now move to multi-stage-docker-build-golang folder

</br >

```
cd multi-stage-docker-build-golang
```
</br >

5. Build your Docker Image 

</br >

```
docker build -t simplecalc-multistage .
```
</br >

6. Verify Docker Image is created

</br >

```
docker images
```

</br >

Output

</br >

```
REPOSITORY        TAG       IMAGE ID       CREATED          SIZE
<none>            <none>    e2e2b395e567   19 minutes ago   647MB
subodhb57/sc-ms   latest    0b1261cccfe5   19 minutes ago   1.96MB
subodhb57/sc      latest    7a503c453499   21 minutes ago   647MB
ubuntu            latest    35a88802559d   12 days ago      78.1MB
hello-world       latest    d2c94e258dcb   13 months ago    13.3kB
```

</br >

We can see that the size of the docker image has drastically reduced my using multi stage docker build method.

</br>

## Here are my snapshots while performing this

</br >

![g1](https://github.com/SubodhBagde/Docker-Project-Hub/assets/136182792/14f11b7c-616f-4eb4-a019-d4ee441d4ea3)

</br >

![g2](https://github.com/SubodhBagde/Docker-Project-Hub/assets/136182792/59024ca6-d587-40f5-b8d9-bace3c72b3fc)

</br >

![g3](https://github.com/SubodhBagde/Docker-Project-Hub/assets/136182792/cf72537c-9db1-403c-a23a-79143b548616)
