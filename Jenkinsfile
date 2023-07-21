pipeline{

agent{

label 'slave'
}

stages{
stage ('stage-1'){
steps{

  //keep these 2 lines uncommented for 1st attempt only.
  
/*sh "docker stop my_cont"
sh "docker system prune -a -f"*/
  sh " yum install java-1.8.0-openjdk-devel.x86_64"
  sh " yum install git -y"
  sh "yum install docker -y"
  sh "systemctl start docker"
  sh "systemctl enable docker"
sh "chmod -R 777 /mnt"
sh "chmod -R 777 /var/run/docker.sock"
sh "docker build -t my_img /mnt/slave/workspace/job2/"
sh "docker run -itdp 651:80 --name my_cont my_img"
sh "docker exec my_cont chmod -R 777 /usr/local/apache2/"

}

}

}
}
