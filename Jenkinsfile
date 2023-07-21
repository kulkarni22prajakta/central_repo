pipeline{

agent{

label 'built-in'
}

stages{
stage ('stage-1'){
steps{

sh "docker build -t my_img /root/.jenkins/workspace/job1/"
sh "docker run -itdp 50:80 --name my_cont my_img"
sh "docker exec my_cont chmod -R 777 /usr/local/apache2/"
}

}

}
}
