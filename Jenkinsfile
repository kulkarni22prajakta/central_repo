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
  sh "sudo su -"
  sh " sudo yum install java-1.8.0-openjdk-devel.x86_64"
  sh " sudo yum install git -y"
  sh "sudo yum install docker -y"
  sh "sudo systemctl start docker"
  sh "sudo systemctl enable docker"
sh "sudo chmod -R 777 /mnt"
sh "sudo chmod -R 777 /var/run/docker.sock"
sh "docker build -t my_img /mnt/slave/workspace/job2/"
sh "docker run -itdp 651:80 --name my_cont my_img"
sh "docker exec my_cont chmod -R 777 /usr/local/apache2/"

}

}

}
}
