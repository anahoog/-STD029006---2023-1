https://hub.docker.com/


aluno: ~$ sudo apt-get update
sudo apt-get install ./docker-desktop-<version>-<arch>.deb

Presumimos que você recebeu as instruções de sempre do administrador
de sistema local. Basicamente, resume-se a estas três coisas:

    #1) Respeite a privacidade dos outros.
    #2) Pense antes de digitar.
    #3) Com grandes poderes vêm grandes responsabilidades.

[sudo] senha para aluno: 
Sinto muito, tente novamente.
[sudo] senha para aluno: 
Sinto muito, usuário aluno não tem permissão para executar "/usr/bin/apt-get update" como root em sj-lin-prog-866462.
bash: version: Arquivo ou diretório inexistente
aluno: ~$ docker

Usage:  docker [OPTIONS] COMMAND

A self-sufficient runtime for containers

Common Commands:
  run         Create and run a new container from an image
  exec        Execute a command in a running container
  ps          List containers
  build       Build an image from a Dockerfile
  pull        Download an image from a registry
  push        Upload an image to a registry
  images      List images
  login       Log in to a registry
  logout      Log out from a registry
  search      Search Docker Hub for images
  version     Show the Docker version information
  info        Display system-wide information

Management Commands:
  builder     Manage builds
  container   Manage containers
  context     Manage contexts
  image       Manage images
  manifest    Manage Docker image manifests and manifest lists
  network     Manage networks
  plugin      Manage plugins
  scan*       Docker Scan (Docker Inc., v0.23.0)
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes

Swarm Commands:
  swarm       Manage Swarm

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  import      Import the contents from a tarball to create a filesystem image
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  wait        Block until one or more containers stop, then print their exit codes

Global Options:
      --config string      Location of client config files (default
                           "/home/aluno/.docker")
  -c, --context string     Name of the context to use to connect to the
                           daemon (overrides DOCKER_HOST env var and
                           default context set with "docker context use")
  -D, --debug              Enable debug mode
  -H, --host list          Daemon socket(s) to connect to
  -l, --log-level string   Set the logging level ("debug", "info",
                           "warn", "error", "fatal") (default "info")
      --tls                Use TLS; implied by --tlsverify
      --tlscacert string   Trust certs signed only by this CA (default
                           "/home/aluno/.docker/ca.pem")
      --tlscert string     Path to TLS certificate file (default
                           "/home/aluno/.docker/cert.pem")
      --tlskey string      Path to TLS key file (default
                           "/home/aluno/.docker/key.pem")
      --tlsverify          Use TLS and verify the remote
  -v, --version            Print version information and quit

Run 'docker COMMAND --help' for more information on a command.

For more help on how to use Docker, head to https://docs.docker.com/go/guides/
aluno: ~$ docker images
REPOSITORY        TAG       IMAGE ID       CREATED       SIZE
imunes/template   latest    f7551ea37a0c   2 weeks ago   815MB
imunes/template   <none>    c009531c75fd   3 years ago   326MB
aluno: ~$ ls
'Área de trabalho'   Downloads   Modelos   Público   Vídeos
 Documentos          Imagens     Música    snap     'VirtualBox VMs'
aluno: ~$ cd Downloads/STD029006---2023-1/
aluno: STD029006---2023-1$ docker run imunes/template
aluno: STD029006---2023-1$ docker run f7551ea37a0c
aluno: STD029006---2023-1$ docker run hello-world
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
2db29710123e: Pull complete 
Digest: sha256:6e8b6f026e0b9c419ea0fd02d3905dd0952ad1feea67543f525c73a0a790fefb
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

aluno: STD029006---2023-1$ docker run -it ubuntu bash
Unable to find image 'ubuntu:latest' locally
latest: Pulling from library/ubuntu
677076032cca: Pull complete 
Digest: sha256:9a0bdde4188b896a372804be2384015e90e3f84906b750c1a53539b585fbbe7f
Status: Downloaded newer image for ubuntu:latest
root@fce0bfed1b96:/# ls
bin   dev  home  lib32  libx32  mnt  proc  run   srv  tmp  var
boot  etc  lib   lib64  media   opt  root  sbin  sys  usr
root@fce0bfed1b96:/# cd home
root@fce0bfed1b96:/home# ls
root@fce0bfed1b96:/home# exit
exit
aluno: STD029006---2023-1$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
aluno: STD029006---2023-1$ docker ps -a
CONTAINER ID   IMAGE             COMMAND       CREATED              STATUS                      PORTS     NAMES
fce0bfed1b96   ubuntu            "bash"        About a minute ago   Exited (0) 38 seconds ago             blissful_rosalind
8b007ff1342e   hello-world       "/hello"      3 minutes ago        Exited (0) 3 minutes ago              fervent_lederberg
ddde9fff81ed   f7551ea37a0c      "/bin/bash"   3 minutes ago        Exited (0) 3 minutes ago              clever_colden
c63e7409b4b3   imunes/template   "/bin/bash"   4 minutes ago        Exited (0) 4 minutes ago              adoring_ishizaka
aluno: STD029006---2023-1$ docker rm ^C
aluno: STD029006---2023-1$ docker rm 8b007ff1342e
8b007ff1342e
aluno: STD029006---2023-1$ docker ps -a
CONTAINER ID   IMAGE             COMMAND       CREATED         STATUS                          PORTS     NAMES
fce0bfed1b96   ubuntu            "bash"        2 minutes ago   Exited (0) About a minute ago             blissful_rosalind
ddde9fff81ed   f7551ea37a0c      "/bin/bash"   4 minutes ago   Exited (0) 4 minutes ago                  clever_colden
c63e7409b4b3   imunes/template   "/bin/bash"   5 minutes ago   Exited (0) 5 minutes ago                  adoring_ishizaka
aluno: STD029006---2023-1$ docker ps -pa
unknown shorthand flag: 'p' in -pa
See 'docker ps --help'.
aluno: STD029006---2023-1$ docker ps -qa
fce0bfed1b96
ddde9fff81ed
c63e7409b4b3
aluno: STD029006---2023-1$ docker rm fce0bfed1b96
ddde9fff81ed
c63e7409b4b3
fce0bfed1b96
bash: ddde9fff81ed: comando não encontrado
bash: c63e7409b4b3: comando não encontrado
aluno: STD029006---2023-1$ docker rm $(docker ps -qa)
ddde9fff81ed
c63e7409b4b3
aluno: STD029006---2023-1$ docker ps -qa
aluno: STD029006---2023-1$ docker image ls
REPOSITORY        TAG       IMAGE ID       CREATED         SIZE
imunes/template   latest    f7551ea37a0c   2 weeks ago     815MB
ubuntu            latest    58db3edaf2be   4 weeks ago     77.8MB
hello-world       latest    feb5d9fea6a5   17 months ago   13.3kB
imunes/template   <none>    c009531c75fd   3 years ago     326MB
aluno: STD029006---2023-1$ docker rmi f7551ea37a0c
Untagged: imunes/template:latest
Deleted: sha256:f7551ea37a0c3c99029db6c600cc08dba0997a40869595e2db0b3ee19d2e454d
Deleted: sha256:0b2ffc1418a1294dcbfa8d027681166bcd42edb7125523561bf1b762349757fa
Deleted: sha256:ca0b051b727a3af95f4e22f164a76c00539f5bd28d1dea320b6672824d1ee8d6
Deleted: sha256:9b68b63f97cb199ebe987bd81b9282735b7a83691341351fbb25cd622a36f112
Deleted: sha256:47de31068bcab76b20fe71d631b45575e9bfbbc120556359c9a7406249e6efe7
Deleted: sha256:a2e1527b5b7a0b999b8199acf91c63c27d297e5f820cff2c18bc5546f1d3051c
Deleted: sha256:bb7b81a625d1914887a39e81589cfa5dc5b637edeef477a89e5dcfc44c5c6724
Deleted: sha256:e79d6ee9dad43704d2539105b9e07f14549cf62e7a8ef392a5c04b481d017177
Deleted: sha256:db055d043dc9f5006cca6bfbaaa1d4072c87b390a7b15fc393e1b276017bcaac
Deleted: sha256:1234a8329fe1d1fd9da5dbb1e4a3272e837da83d5e3e2e90d8158f64ee3ef62c
Deleted: sha256:54a402dda985dbbd3e352f8f324608f2051070115f4f296d588b7cddbcdb54bf
Deleted: sha256:66463bc23517ad4776cebbe9e010007cc7555b57693bbd2dad7689cc1e0d5b70
Deleted: sha256:800a2e8ebe8365731e5da963f44222460b4e9e74bfd924c09ad2b84ab7b97a43
Deleted: sha256:c957c2773adedaa1d7e0b8a875659c655d6c27e008569a22ab005a95dbafd071
Deleted: sha256:0e9733d8de35290fd070e4b0ea71e737022d0ab82f903c6576797834fbe1af13
Deleted: sha256:ed3ebd2296825334a7c9cdac25af15443cc2977cb2e21356aca7a39dd632f888
Deleted: sha256:8d2dfc26182d08002c257c4e681bb053a355e56cb0c0017d4903a11470e5baa9
Deleted: sha256:dd54b82ecbf86ba20979c43fed9121d2e87cd6b800e854167e2d0de2b936a661
Deleted: sha256:edcb5acc225c82d04f34187a125df8066684625bd3183a333556fae979d86fa0
Deleted: sha256:4836511b3c8f07095158696b60a6fc1a344f710471361929e4353aa421747eaa
Deleted: sha256:c2a4ef69b251576020cdab52b62de431a6212d377c960599d28a83009249cdf8
Deleted: sha256:ce7da4031a1443e7df7901102dddc6d12f547d76e737f30eddca213c5ed2ea47
Deleted: sha256:4fecf7152b21f30e815bfa6e5f968a5cc3a97f4b7453ba52a16e4c4ccb57417f
Deleted: sha256:92fadc93c4e90b83f6ce49c8fa262c5aac66d74f414ae1f9a75fd5b2986acd26
Deleted: sha256:e41158c5dfbedd5819d1b44cbbe7a5250b755fa557e29ce2c4fc098b75165b77
Deleted: sha256:7f3e8f969df202c81a93d4fddc567945837bd38cd937917bf0b27545ac7451e1
Deleted: sha256:3a11b51ba123603df225aa6633361d8416f91492e2e5a8c56196cbd51c5cb3c6
Deleted: sha256:d3501d32fe682d53dd793ba04731459d71a0f14bf2274f2267d19099ce2e665a
Deleted: sha256:4f185b4da6658721fd9874b2093f5a21de04048263825b592217d1b51380585b
Deleted: sha256:6b2cb6e26ed4568807956cdc747b46e96430e2aaa39f6d4ffa2754719a4e2786
aluno: STD029006---2023-1$ docker image ls
REPOSITORY        TAG       IMAGE ID       CREATED         SIZE
ubuntu            latest    58db3edaf2be   4 weeks ago     77.8MB
hello-world       latest    feb5d9fea6a5   17 months ago   13.3kB
imunes/template   <none>    c009531c75fd   3 years ago     326MB
aluno: STD029006---2023-1$ docker rmi c009531c75fd
Untagged: imunes/template@sha256:2df4a217f4e0be31c231c7682c1a9be1a99d299e6f09ef64a1aa4f95cd0b54e5
Deleted: sha256:c009531c75fdd74ce1550cc52c66b3d34da1710d6c04efff51f013af4de14941
Deleted: sha256:ed8127367ac8b2ee6a9e897846ca386460894da9312915499ec1620254564e34
Deleted: sha256:070600ea76287c9c0b712eb3113c01b893c7ba931b826edbac481b611d3d8fc4
Deleted: sha256:9c8235891167137783c56f2a87dd1068296c75c5b731e379350eb201a1b12024
Deleted: sha256:8a65dde437406e5c58944031cb9f83f37cc5d7aa44cd4487d6e4077336e701b0
Deleted: sha256:8afb304ad96e62a1282c4e2e9e084f86c35f08ecbe19f0c0bdb6ebac43bd83cd
Deleted: sha256:38b43c5bd92c10daabfd50e7fb68c5b1eb5e040ea1264c88961eed0d0e7a33da
Deleted: sha256:fbb641a8b94349e89886f65d79928e4673530e2a2b4d33c2c95e0426713f78e4
aluno: STD029006---2023-1$ docker rmi feb5d9fea6a5
Untagged: hello-world:latest
Untagged: hello-world@sha256:6e8b6f026e0b9c419ea0fd02d3905dd0952ad1feea67543f525c73a0a790fefb
Deleted: sha256:feb5d9fea6a5e9606aa995e879d862b825965ba48de054caab5ef356dc6b3412
Deleted: sha256:e07ee1baac5fae6a26f30cabfe54a36d3402f96afda318fe0a96cec4ca393359
aluno: STD029006---2023-1$ docker image ls
REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
ubuntu       latest    58db3edaf2be   4 weeks ago   77.8MB
aluno: STD029006---2023-1$ docker run -it --rm ubuntu bash
root@85f7a36fef39:/# exit
exit
aluno: STD029006---2023-1$ docker image ls
REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
ubuntu       latest    58db3edaf2be   4 weeks ago   77.8MB
aluno: STD029006---2023-1$ docker ps -qa
aluno: STD029006---2023-1$ docker run -it --rm ubuntu bash
root@f58016a2a90b:/# java
bash: java: command not found
root@f58016a2a90b:/# chrome
bash: chrome: command not found
root@f58016a2a90b:/# ls
bin   dev  home  lib32  libx32  mnt  proc  run   srv  tmp  var
boot  etc  lib   lib64  media   opt  root  sbin  sys  usr
root@f58016a2a90b:/# apt get install java
E: Invalid operation get
root@f58016a2a90b:/# aptget install java
bash: aptget: command not found
root@f58016a2a90b:/# exit
exit
aluno: STD029006---2023-1$ docker search openjdk
NAME                            DESCRIPTION                                     STARS     OFFICIAL   AUTOMATED
openjdk                         Pre-release / non-production builds of OpenJ…   3581      [OK]       
eclipse-temurin                 Official Images for OpenJDK binaries built b…   287       [OK]       
ibm-semeru-runtimes             IBM Semeru Runtimes Official Images for Open…   25        [OK]       
circleci/openjdk                CircleCI images for OpenJDK                     11                   [OK]
cimg/openjdk                    The CircleCI OpenJDK (Java) Docker Convenien…   4                    
clearlinux/openjdk              OpenJDK implementation of the Java Platform …   2                    
noenv/openjdk                   OpenJDK Docker Image                            0                    
jenkins/openjdk                  Docker Images based on various AdoptOpenJDK…   0                    
clarinpl/openjdk                                                                0                    
clarinpl/openjdk-jre                                                            0                    
adoptopenjdk/openjdk11          Docker Images for OpenJDK Version 11 binarie…   212                  
adoptopenjdk/openjdk8           Docker Images for OpenJDK Version 8 binaries…   129                  
cfje/openjdk                    OpenJDK Builder Image                           0                    
adoptopenjdk/openjdk16          Docker Images for OpenJDK Version 16 binarie…   17                   
amd64/openjdk                   Pre-release / non-production builds of OpenJ…   11                   
adoptopenjdk/openjdk15          Docker Images for OpenJDK Version 15 binarie…   10                   
adoptopenjdk/openjdk14          Docker Images for OpenJDK Version 14 binarie…   11                   
suranagivinod/openjdk8          openjdk:8-jre-slim, zip & unzip                 2                    
adoptopenjdk/openjdk13          Docker Images for OpenJDK Version 13 binarie…   11                   
winamd64/openjdk                Pre-release / non-production builds of OpenJ…   21                   
arm64v8/openjdk                 Pre-release / non-production builds of OpenJ…   49                   
adoptopenjdk/openjdk12          Docker Images for OpenJDK Version 12 binarie…   17                   
classmethod/openjdk-with-git    docker image for openjdk and git                1                    [OK]
adoptopenjdk/openjdk11-openj9   Docker Images for Eclipse OpenJ9 Version 11 …   50                   
symphonicsoft/openjdkbase       Openjdk base images with dumb-init              1                    
aluno: STD029006---2023-1$ docker run -it eclipse-temurin bash
Unable to find image 'eclipse-temurin:latest' locally
latest: Pulling from library/eclipse-temurin
10ac4908093d: Pull complete 
6df15e605e38: Pull complete 
e42801c1d39d: Pull complete 
ecafd6200f88: Pull complete 
Digest: sha256:a0901c0803060995ca6e13d19756e3100987101ac33e3d7eb091d5477374282c
Status: Downloaded newer image for eclipse-temurin:latest
root@d015b3babff5:/# java -version
openjdk version "19.0.2" 2023-01-17
OpenJDK Runtime Environment Temurin-19.0.2+7 (build 19.0.2+7)
OpenJDK 64-Bit Server VM Temurin-19.0.2+7 (build 19.0.2+7, mixed mode, sharing)
root@d015b3babff5:/# java
Usage: java [options] <mainclass> [args...]
           (to execute a class)
   or  java [options] -jar <jarfile> [args...]
           (to execute a jar file)
   or  java [options] -m <module>[/<mainclass>] [args...]
       java [options] --module <module>[/<mainclass>] [args...]
           (to execute the main class in a module)
   or  java [options] <sourcefile> [args]
           (to execute a single source-file program)

 Arguments following the main class, source file, -jar <jarfile>,
 -m or --module <module>/<mainclass> are passed as the arguments to
 main class.

 where options include:

    -cp <class search path of directories and zip/jar files>
    -classpath <class search path of directories and zip/jar files>
    --class-path <class search path of directories and zip/jar files>
                  A : separated list of directories, JAR archives,
                  and ZIP archives to search for class files.
    -p <module path>
    --module-path <module path>...
                  A : separated list of directories, each directory
                  is a directory of modules.
    --upgrade-module-path <module path>...
                  A : separated list of directories, each directory
                  is a directory of modules that replace upgradeable
                  modules in the runtime image
    --add-modules <module name>[,<module name>...]
                  root modules to resolve in addition to the initial module.
                  <module name> can also be ALL-DEFAULT, ALL-SYSTEM,
                  ALL-MODULE-PATH.
    --enable-native-access <module name>[,<module name>...]
                  modules that are permitted to perform restricted native operations.
                  <module name> can also be ALL-UNNAMED.
    --list-modules
                  list observable modules and exit
    -d <module name>
    --describe-module <module name>
                  describe a module and exit
    --dry-run     create VM and load main class but do not execute main method.
                  The --dry-run option may be useful for validating the
                  command-line options such as the module system configuration.
    --validate-modules
                  validate all modules and exit
                  The --validate-modules option may be useful for finding
                  conflicts and other errors with modules on the module path.
    -D<name>=<value>
                  set a system property
    -verbose:[class|module|gc|jni]
                  enable verbose output for the given subsystem
    -version      print product version to the error stream and exit
    --version     print product version to the output stream and exit
    -showversion  print product version to the error stream and continue
    --show-version
                  print product version to the output stream and continue
    --show-module-resolution
                  show module resolution output during startup
    -? -h -help
                  print this help message to the error stream
    --help        print this help message to the output stream
    -X            print help on extra options to the error stream
    --help-extra  print help on extra options to the output stream
    -ea[:<packagename>...|:<classname>]
    -enableassertions[:<packagename>...|:<classname>]
                  enable assertions with specified granularity
    -da[:<packagename>...|:<classname>]
    -disableassertions[:<packagename>...|:<classname>]
                  disable assertions with specified granularity
    -esa | -enablesystemassertions
                  enable system assertions
    -dsa | -disablesystemassertions
                  disable system assertions
    -agentlib:<libname>[=<options>]
                  load native agent library <libname>, e.g. -agentlib:jdwp
                  see also -agentlib:jdwp=help
    -agentpath:<pathname>[=<options>]
                  load native agent library by full pathname
    -javaagent:<jarpath>[=<options>]
                  load Java programming language agent, see java.lang.instrument
    -splash:<imagepath>
                  show splash screen with specified image
                  HiDPI scaled images are automatically supported and used
                  if available. The unscaled image filename, e.g. image.ext,
                  should always be passed as the argument to the -splash option.
                  The most appropriate scaled image provided will be picked up
                  automatically.
                  See the SplashScreen API documentation for more information
    @argument files
                  one or more argument files containing options
    -disable-@files
                  prevent further argument file expansion
    --enable-preview
                  allow classes to depend on preview features of this release
To specify an argument for a long option, you can use --<name>=<value> or
--<name> <value>.

root@d015b3babff5:/# .java
bash: .java: command not found
root@d015b3babff5:/# /java
bash: /java: No such file or directory
root@d015b3babff5:/# exit
exit
aluno: STD029006---2023-1$ docker ps -qa
d015b3babff5
aluno: STD029006---2023-1$ docker image ls
REPOSITORY        TAG       IMAGE ID       CREATED       SIZE
eclipse-temurin   latest    9db449eeaabb   4 weeks ago   472MB
ubuntu            latest    58db3edaf2be   4 weeks ago   77.8MB
aluno: STD029006---2023-1$ docker run -it alpine ash
Unable to find image 'alpine:latest' locally
latest: Pulling from library/alpine
63b65145d645: Pull complete 
Digest: sha256:69665d02cb32192e52e07644d76bc6f25abeb5410edc1c7a81a10ba3f0efb90a
Status: Downloaded newer image for alpine:latest
/ # exit
aluno: STD029006---2023-1$ docker run -it --name std alpine ash
/ # exit
aluno: STD029006---2023-1$ docker image ls
REPOSITORY        TAG       IMAGE ID       CREATED       SIZE
alpine            latest    b2aa39c304c2   2 weeks ago   7.05MB
eclipse-temurin   latest    9db449eeaabb   4 weeks ago   472MB
ubuntu            latest    58db3edaf2be   4 weeks ago   77.8MB
aluno: STD029006---2023-1$ docker ps -qa
37993676a79c
5e121142ca44
d015b3babff5
aluno: STD029006---2023-1$ docker run -it --name std alpine ash
docker: Error response from daemon: Conflict. The container name "/std" is already in use by container "37993676a79cf18c403699ce89fa8afe790ae42a6852701a55cf062edbd97d0b". You have to remove (or rename) that container to be able to reuse that name.
See 'docker run --help'.
aluno: STD029006---2023-1$ docker rm $(docker ps -qa)
37993676a79c
5e121142ca44
d015b3babff5
aluno: STD029006---2023-1$ docker ps -qa
aluno: STD029006---2023-1$ docker run -it --name std alpine ash
/ # exit
aluno: STD029006---2023-1$ docker ps -qa
797a10b750bc
aluno: STD029006---2023-1$ docker run -it --name std alpine bash
docker: Error response from daemon: Conflict. The container name "/std" is already in use by container "797a10b750bc9a704fb91d693dce19c6c931e30c93e9d6f83ab1f1bf02873669". You have to remove (or rename) that container to be able to reuse that name.
See 'docker run --help'.
aluno: STD029006---2023-1$ docker rm $(docker ps -qa)
797a10b750bc
aluno: STD029006---2023-1$ docker run -it --name std alpine bash
docker: Error response from daemon: failed to create shim task: OCI runtime create failed: runc create failed: unable to start container process: exec: "bash": executable file not found in $PATH: unknown.
ERRO[0000] error waiting for container: context canceled 
aluno: STD029006---2023-1$ docker ps -qa
f8d9b432d85f
aluno: STD029006---2023-1$ docker rm $(docker ps -qa)
f8d9b432d85f
aluno: STD029006---2023-1$ docker run -it --name std ubuntu bash
root@62dd533ed93e:/# exit
exit
aluno: STD029006---2023-1$ docker ps -qa
62dd533ed93e
aluno: STD029006---2023-1$ docker ps -qa
62dd533ed93e
aluno: STD029006---2023-1$ docker rm $(docker ps -qa)
62dd533ed93e
aluno: STD029006---2023-1$ docker ps -qa
aluno: STD029006---2023-1$ docker run -it --name std ubuntu bash
root@97b132c526ee:/# exit
exit
aluno: STD029006---2023-1$ docker ps 
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
aluno: STD029006---2023-1$ echo "ola mundo" ola.txt
ola mundo ola.txt
aluno: STD029006---2023-1$ echo "ola mundo"> ola.txt
aluno: STD029006---2023-1$ ls -l
total 12
drwxr-xr-x 2 aluno aluno 4096 fev 28 17:02 'Lab 01'
-rw-r--r-- 1 aluno aluno   10 fev 28 17:21  ola.txt
-rw-r--r-- 1 aluno aluno   42 fev 28 16:45  README.md
aluno: STD029006---2023-1$ docker run -it --name std ubuntu bash
docker: Error response from daemon: Conflict. The container name "/std" is already in use by container "97b132c526ee390c62227bf93c140ecc5554d7dc35074dc9de2d878fcd6a5841". You have to remove (or rename) that container to be able to reuse that name.
See 'docker run --help'.
aluno: STD029006---2023-1$ docker run -it  std ubuntu bash
Unable to find image 'std:latest' locally
docker: Error response from daemon: pull access denied for std, repository does not exist or may require 'docker login': denied: requested access to the resource is denied.
See 'docker run --help'.
aluno: STD029006---2023-1$ docker rm $(docker ps -qa)
97b132c526ee
aluno: STD029006---2023-1$ docker run -it --name std ubuntu bash
root@d8f268093a3c:/# exit
exit
aluno: STD029006---2023-1$ docker run -it -v $(pwd):/app --name std ubuntu bash
docker: Error response from daemon: Conflict. The container name "/std" is already in use by container "d8f268093a3c263820878991b9366ab6618857329d7f7458e9516730a3e2b097". You have to remove (or rename) that container to be able to reuse that name.
See 'docker run --help'.
aluno: STD029006---2023-1$ docker rm $(docker ps -qa)
d8f268093a3c
aluno: STD029006---2023-1$ docker run -it -v $(pwd):/app --name std ubuntu bash
root@1f985707c214:/# ls
app  bin  boot  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@1f985707c214:/# cd app
root@1f985707c214:/app# ls
'Lab 01'   README.md   ola.txt
root@1f985707c214:/app# echo "novo" > novo.txt
root@1f985707c214:/app# ls
'Lab 01'   README.md   novo.txt   ola.txt
root@1f985707c214:/app# 
