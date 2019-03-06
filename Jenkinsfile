node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t webdev:V1 ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'bosek83' -p 'Calvary83#' "
sh "docker tag webdev:V1 bosek83/galilee:V1"
sh "docker push bosek83/galilee:V1"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
