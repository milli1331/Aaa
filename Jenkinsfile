pipeline{
agent any
tools{
maven 'Maven'
}
stages{
stage('Checkout'){
steps{
git branch:'master',url:'https://github.com/milli1331/Aaa.git'
}
}
stage('Build'){
steps{
sh 'mvn clean package'
}
}
stage('Test'){
steps{
sh 'mvn Test'
}
}
stage('Run application'){
steps{
sh 'java -jar target/milli-1.0-SNAPSHOT.jar'
}
}
}
post{
success{
echo 'syuccess'
}
failure{
echo 'failed'
}
}
}
