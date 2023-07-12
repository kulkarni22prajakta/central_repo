pipeline{

agent{

label 'built-in'
}

stages{
stage ('stage-1'){
steps{

sh "cp -r index.html /var/www/html/"
sh "chmod -R 777 /var/www/html"
}

}

}
}
