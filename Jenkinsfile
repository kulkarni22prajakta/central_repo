pipeline{

agent{

label 'slave'
}

stages{
stage ('stage-1'){
steps{
/*sh "docker stop my_cont"*/
sh "docker system prune -a -f"
sh "docker build -t my_img /mnt/slave/workspace/job2/"
sh "docker run -itdp 651:80 --name my_cont my_img"
sh "docker exec my_cont chmod -R 777 /usr/local/apache2/"

}

}

}
}
