pipeline{

agent{

label 'built-in'
}

stages{
stage ('stage-1'){
steps{

sh "docker build -t my_img /root/.jenkins/workspace/job1/"
sh "docker run -itdp 651:80 --name my_cont2 my_img"
sh "docker exec my_cont2 chmod -R 777 /usr/local/apache2/"
}

}

}
}
