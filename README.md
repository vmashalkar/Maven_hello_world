            yum install wget -y
                #----------------Install jdk from browser---------------------
                wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u192-b12/750e1c8617c5452694857ad95c3ee230/jdk-8u192-linux-x64.tar.gz
                #-------------untar jdk file--------
                        tar -xvf jdk-8u192-linux-x64.tar.gz
                        echo "JDK installed"
                        export JAVA_HOME=$(find / -type d -name "jdk1.8.0_192")
                        echo "java path ="$JAVA_HOME
                        export PATH=$PATH:$JAVA_HOME/bin
                        echo "whole path ="$PATH
                        sleep 10s
                        echo  "Total java installed successfully"
                        yum install git
                        wget http://mirror.olnevhost.net/pub/apache/maven/maven-3/3.0.5/binaries/apache-maven-3.0.5-bin.tar.gz
                        tar -xvf apache-maven-3.0.5-bin.tar.gz
                        export MAVEN_HOME=$(find / -type d -name "apache-maven-3.0.5")
                        export PATH=$PATH:$MAVEN_HOME/bin
                        echo "whole path ="$PATH
                        sleep 10s
                        git clone "https://github.com/pdurbin/maven-hello-world.git"
                        a=$(find / -type d -name "maven-hello-world")
                        cd $a/my-app
                        mvn clean install

