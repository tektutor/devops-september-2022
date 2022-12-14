# Devops September 2022 ( 26-30 Sep 2022 )

## Day 1

## Installing JDK 17 in CentOS 7.9 2009
```
cd ~/Downloads
wget https://download.oracle.com/java/17/latest/jdk-17_linux-x64_bin.rpm 
sudo yum install -y jdk-17_linux-x64_bin.rpm
```

Expected output
<pre>
[jegan@tektutor.org ~]$ <b>cd Downloads/</b>
[jegan@tektutor.org Downloads]$ <b>wget https://download.oracle.com/java/17/latest/jdk-17_linux-x64_bin.rpm</b>
--2022-09-25 22:21:46--  https://download.oracle.com/java/17/latest/jdk-17_linux-x64_bin.rpm
Resolving download.oracle.com (download.oracle.com)... 23.1.36.114
Connecting to download.oracle.com (download.oracle.com)|23.1.36.114|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 162804836 (155M) [application/x-redhat-package-manager]
Saving to: ‘jdk-17_linux-x64_bin.rpm’

100%[===========================================================>] 162,804,836 11.3MB/s   in 14s    

2022-09-25 22:22:01 (10.9 MB/s) - ‘jdk-17_linux-x64_bin.rpm’ saved [162804836/162804836]

[jegan@tektutor.org Downloads]$ sudo yum install ./jdk-17_linux-x64_bin.rpm 
Loaded plugins: fastestmirror, langpacks
Examining ./jdk-17_linux-x64_bin.rpm: 2000:jdk-17-17.0.4.1-ga.x86_64
Marking ./jdk-17_linux-x64_bin.rpm to be installed
Resolving Dependencies
--> Running transaction check
---> Package jdk-17.x86_64 2000:17.0.4.1-ga will be installed
--> Finished Dependency Resolution

Dependencies Resolved

=====================================================================================================
 Package          Arch             Version                     Repository                       Size
=====================================================================================================
Installing:
 jdk-17           x86_64           2000:17.0.4.1-ga            /jdk-17_linux-x64_bin           302 M

Transaction Summary
=====================================================================================================
Install  1 Package

Total size: 302 M
Installed size: 302 M
Is this ok [y/d/N]: y
Downloading packages:
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Installing : 2000:jdk-17-17.0.4.1-ga.x86_64                                                    1/1 
  Verifying  : 2000:jdk-17-17.0.4.1-ga.x86_64                                                    1/1 

Installed:
  jdk-17.x86_64 2000:17.0.4.1-ga                                                                     

Complete!

[jegan@tektutor.org Downloads]$ <b>javac -version</b>
javac 17.0.4.1
[jegan@tektutor.org Downloads]$ <b>java -version</b>
java version "17.0.4.1" 2022-08-18 LTS
Java(TM) SE Runtime Environment (build 17.0.4.1+1-LTS-2)
Java HotSpot(TM) 64-Bit Server VM (build 17.0.4.1+1-LTS-2, mixed mode, sharing)
</pre>


## Installing Apache Maven in CentOS 7.9 2009
```
cd ~/Downloads
wget https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz --no-check-certificate
tar xvfz apache-maven-3.8.6-bin.tar.gz 
mvn --version
```

Expected output
<pre>
[jegan@tektutor.org Downloads]$ <b>wget https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz --no-check-certificate</b>
--2022-09-25 22:25:33--  https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz
Resolving dlcdn.apache.org (dlcdn.apache.org)... 151.101.2.132, 2a04:4e42::644
Connecting to dlcdn.apache.org (dlcdn.apache.org)|151.101.2.132|:443... connected.
WARNING: cannot verify dlcdn.apache.org's certificate, issued by ‘/C=US/O=Let's Encrypt/CN=R3’:
  Issued certificate has expired.
HTTP request sent, awaiting response... 200 OK
Length: 8676320 (8.3M) [application/x-gzip]
Saving to: ‘apache-maven-3.8.6-bin.tar.gz’

100%[===========================================================>] 8,676,320   10.5MB/s   in 0.8s   

2022-09-25 22:25:34 (10.5 MB/s) - ‘apache-maven-3.8.6-bin.tar.gz’ saved [8676320/8676320]

[jegan@tektutor.org Downloads]$ <b>ls</b>
apache-maven-3.8.6-bin.tar.gz  google-chrome-stable_current_x86_64.rpm  jdk-17_linux-x64_bin.rpm
[jegan@tektutor.org Downloads]$ <b>tar xvfz apache-maven-3.8.6-bin.tar.gz</b>
apache-maven-3.8.6/README.txt
apache-maven-3.8.6/LICENSE
apache-maven-3.8.6/NOTICE
apache-maven-3.8.6/lib/
apache-maven-3.8.6/lib/commons-cli.license
apache-maven-3.8.6/lib/commons-io.license
apache-maven-3.8.6/lib/commons-lang3.license
apache-maven-3.8.6/lib/guava.license
apache-maven-3.8.6/lib/guice.license
apache-maven-3.8.6/lib/jansi.license
apache-maven-3.8.6/lib/javax.annotation-api.license
apache-maven-3.8.6/lib/javax.inject.license
apache-maven-3.8.6/lib/jcl-over-slf4j.license
apache-maven-3.8.6/lib/org.eclipse.sisu.inject.license
apache-maven-3.8.6/lib/org.eclipse.sisu.plexus.license
apache-maven-3.8.6/lib/plexus-cipher.license
apache-maven-3.8.6/lib/plexus-component-annotations.license
apache-maven-3.8.6/lib/plexus-interpolation.license
apache-maven-3.8.6/lib/plexus-sec-dispatcher.license
apache-maven-3.8.6/lib/plexus-utils.license
apache-maven-3.8.6/lib/slf4j-api.license
apache-maven-3.8.6/boot/
apache-maven-3.8.6/boot/plexus-classworlds.license
apache-maven-3.8.6/lib/jansi-native/
apache-maven-3.8.6/lib/jansi-native/Windows/
apache-maven-3.8.6/lib/jansi-native/Windows/x86/
apache-maven-3.8.6/lib/jansi-native/Windows/x86_64/
apache-maven-3.8.6/lib/jansi-native/Windows/x86/jansi.dll
apache-maven-3.8.6/lib/jansi-native/Windows/x86_64/jansi.dll
apache-maven-3.8.6/bin/m2.conf
apache-maven-3.8.6/bin/mvn.cmd
apache-maven-3.8.6/bin/mvnDebug.cmd
apache-maven-3.8.6/bin/mvn
apache-maven-3.8.6/bin/mvnDebug
apache-maven-3.8.6/bin/mvnyjp
apache-maven-3.8.6/conf/
apache-maven-3.8.6/conf/logging/
apache-maven-3.8.6/conf/logging/simplelogger.properties
apache-maven-3.8.6/conf/settings.xml
apache-maven-3.8.6/conf/toolchains.xml
apache-maven-3.8.6/lib/ext/
apache-maven-3.8.6/lib/jansi-native/
apache-maven-3.8.6/lib/ext/README.txt
apache-maven-3.8.6/lib/jansi-native/README.txt
apache-maven-3.8.6/boot/plexus-classworlds-2.6.0.jar
apache-maven-3.8.6/lib/maven-embedder-3.8.6.jar
apache-maven-3.8.6/lib/maven-settings-3.8.6.jar
apache-maven-3.8.6/lib/maven-settings-builder-3.8.6.jar
apache-maven-3.8.6/lib/maven-plugin-api-3.8.6.jar
apache-maven-3.8.6/lib/maven-model-3.8.6.jar
apache-maven-3.8.6/lib/maven-model-builder-3.8.6.jar
apache-maven-3.8.6/lib/maven-builder-support-3.8.6.jar
apache-maven-3.8.6/lib/maven-resolver-api-1.6.3.jar
apache-maven-3.8.6/lib/maven-resolver-util-1.6.3.jar
apache-maven-3.8.6/lib/maven-shared-utils-3.3.4.jar
apache-maven-3.8.6/lib/commons-io-2.6.jar
apache-maven-3.8.6/lib/guice-4.2.2-no_aop.jar
apache-maven-3.8.6/lib/guava-25.1-android.jar
apache-maven-3.8.6/lib/javax.inject-1.jar
apache-maven-3.8.6/lib/javax.annotation-api-1.2.jar
apache-maven-3.8.6/lib/plexus-utils-3.3.1.jar
apache-maven-3.8.6/lib/plexus-sec-dispatcher-2.0.jar
apache-maven-3.8.6/lib/plexus-cipher-2.0.jar
apache-maven-3.8.6/lib/slf4j-api-1.7.36.jar
apache-maven-3.8.6/lib/commons-lang3-3.8.1.jar
apache-maven-3.8.6/lib/maven-core-3.8.6.jar
apache-maven-3.8.6/lib/maven-repository-metadata-3.8.6.jar
apache-maven-3.8.6/lib/maven-artifact-3.8.6.jar
apache-maven-3.8.6/lib/maven-resolver-provider-3.8.6.jar
apache-maven-3.8.6/lib/maven-resolver-impl-1.6.3.jar
apache-maven-3.8.6/lib/maven-resolver-spi-1.6.3.jar
apache-maven-3.8.6/lib/org.eclipse.sisu.inject-0.3.5.jar
apache-maven-3.8.6/lib/plexus-interpolation-1.26.jar
apache-maven-3.8.6/lib/plexus-component-annotations-2.1.0.jar
apache-maven-3.8.6/lib/maven-compat-3.8.6.jar
apache-maven-3.8.6/lib/wagon-provider-api-3.5.1.jar
apache-maven-3.8.6/lib/org.eclipse.sisu.plexus-0.3.5.jar
apache-maven-3.8.6/lib/commons-cli-1.4.jar
apache-maven-3.8.6/lib/wagon-http-3.5.1-shaded.jar
apache-maven-3.8.6/lib/jcl-over-slf4j-1.7.36.jar
apache-maven-3.8.6/lib/wagon-file-3.5.1.jar
apache-maven-3.8.6/lib/maven-resolver-connector-basic-1.6.3.jar
apache-maven-3.8.6/lib/maven-resolver-transport-wagon-1.6.3.jar
apache-maven-3.8.6/lib/maven-slf4j-provider-3.8.6.jar
apache-maven-3.8.6/lib/jansi-2.4.0.jar
[jegan@tektutor.org Downloads]$ cd apache-maven-3.8.6/
[jegan@tektutor.org apache-maven-3.8.6]$ ls
bin  boot  conf  lib  LICENSE  NOTICE  README.txt
[jegan@tektutor.org apache-maven-3.8.6]$ pwd
/home/jegan/Downloads/apache-maven-3.8.6
[jegan@tektutor.org apache-maven-3.8.6]$ vim ~/.bashrc
[jegan@tektutor.org apache-maven-3.8.6]$ source ~/.bashrc
[jegan@tektutor.org apache-maven-3.8.6]$ cd ~
[jegan@tektutor.org ~]$ pwd
/home/jegan
[jegan@tektutor.org ~]$ <b>mvn --version</b>
Apache Maven 3.8.6 (84538c9988a25aec085021c365c560670ad80f63)
Maven home: /home/jegan/Downloads/apache-maven-3.8.6
Java version: 17.0.4.1, vendor: Oracle Corporation, runtime: /usr/java/jdk-17.0.4.1
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "3.10.0-1160.el7.x86_64", arch: "amd64", family: "unix"
</pre>

## Cloning TekTutor GitHub Repo
```
cd ~
git clone https://github.com/tektutor/devops-september-2022.git
cd devops-september-2022
ls
```

Expected output
<pre>
[jegan@tektutor.org ~]$ <b>git clone https://github.com/tektutor/devops-september-2022.git</b>
Cloning into 'devops-september-2022'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 12 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (12/12), done.
</pre>

## Pulling delta changes done after you had cloned
```
cd ~/dev
```

Expected output
<pre>
[jegan@tektutor.org devops-september-2022]$ git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/tektutor/devops-september-2022
   33a1413..0286e87  main       -> origin/main
Updating 33a1413..0286e87
Fast-forward
 README.md | 19 +++++++++++++++++++
 1 file changed, 19 insertions(+)
</pre>

## Installing Docker Community Edition in CentOS 7.9
```
sudo yum install -y yum-utils

sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

sudo yum install docker-ce docker-ce-cli containerd.io docker-compose-plugin

sudo systemctl enable docker
sudo systemctl start docker
sudo usermod -aG docker $USER
newgrp docker
```

Expected output
<pre>
[jegan@tektutor.org Day1]$ <b>sudo systemctl status docker</b>
● docker.service - Docker Application Container Engine
   Loaded: loaded (/usr/lib/systemd/system/docker.service; enabled; vendor preset: disabled)
   Active: inactive (dead)
     Docs: https://docs.docker.com
[jegan@tektutor.org Day1]$ <b>sudo systemctl start docker</b>
[jegan@tektutor.org Day1]$ sudo systemctl status docker
● docker.service - Docker Application Container Engine
   Loaded: loaded (/usr/lib/systemd/system/docker.service; enabled; vendor preset: disabled)
   Active: active (running) since Mon 2022-09-26 04:45:53 PDT; 1s ago
     Docs: https://docs.docker.com
 Main PID: 94070 (dockerd)
    Tasks: 9
   Memory: 30.3M
   CGroup: /system.slice/docker.service
           └─94070 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock

Sep 26 04:45:51 tektutor.org dockerd[94070]: time="2022-09-26T04:45:51.703558501-07:00" level=info msg="ccResolve...=grpc
Sep 26 04:45:51 tektutor.org dockerd[94070]: time="2022-09-26T04:45:51.703565751-07:00" level=info msg="ClientCon...=grpc
Sep 26 04:45:51 tektutor.org dockerd[94070]: time="2022-09-26T04:45:51.721524912-07:00" level=info msg="Loading c...art."
Sep 26 04:45:52 tektutor.org dockerd[94070]: time="2022-09-26T04:45:52.757913645-07:00" level=info msg="Default b...ress"
Sep 26 04:45:52 tektutor.org dockerd[94070]: time="2022-09-26T04:45:52.935855433-07:00" level=info msg="Firewalld...ning"
Sep 26 04:45:53 tektutor.org dockerd[94070]: time="2022-09-26T04:45:53.129260905-07:00" level=info msg="Loading c...one."
Sep 26 04:45:53 tektutor.org dockerd[94070]: time="2022-09-26T04:45:53.158376476-07:00" level=info msg="Docker da...10.18
Sep 26 04:45:53 tektutor.org dockerd[94070]: time="2022-09-26T04:45:53.158709003-07:00" level=info msg="Daemon ha...tion"
Sep 26 04:45:53 tektutor.org systemd[1]: Started Docker Application Container Engine.
Sep 26 04:45:53 tektutor.org dockerd[94070]: time="2022-09-26T04:45:53.215227250-07:00" level=info msg="API liste...sock"
Hint: Some lines were ellipsized, use -l to show in full.
[jegan@tektutor.org Day1]$ <b>docker images</b>
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/images/json": dial unix /var/run/docker.sock: connect: permission denied
[jegan@tektutor.org Day1]$ <b>id</b>
uid=1000(jegan) gid=1000(jegan) groups=1000(jegan) context=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023
[jegan@tektutor.org Day1]$ <b>echo $USER</b>
jegan
[jegan@tektutor.org Day1]$ <b>sudo usermod -aG docker $USER</b>
[jegan@tektutor.org Day1]$ <b>id</b>
uid=1000(jegan) gid=1000(jegan) groups=1000(jegan) context=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023
[jegan@tektutor.org Day1]$ <b>newgrp docker</b>
[jegan@tektutor.org Day1]$ id
uid=1000(jegan) gid=981(docker) groups=981(docker),1000(jegan) context=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023

[jegan@tektutor.org Day1]$ <b>docker images</b>
REPOSITORY   TAG       IMAGE ID   CREATED   SIZE
</pre>
