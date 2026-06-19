pipeline{
agent any
tools{
maven 'Maven'
jdk 'JDK'
}
stages{
stage('Checkout'){
steps{
git branch:'master',url:'https://github.com/bitcsedevops200/mvnsel.git'
}
}

stage('Build'){
steps{
sh'mvn clean package'
}
}

stage('Test'){
steps{
sh'mvn test'
}
}
}
post{
success{
echo'build and development successful'
}
failure{
echo'build failed'
}
}
}
