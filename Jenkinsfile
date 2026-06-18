pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
		}
	stages{
		stage('checkout'){
			git branch:'main', url:'https://github.com/tanush-02/gradleE.git'
			}
		stage('build'){
			sh 'gradle build'
			}
		stage('test'){
			sh 'gradle test'
			}
		stage('Run application'){
			sh 'gradle run'
			}
		}
	post{
		success{
			echo "Build Successful"
			}
		failure{
			echo "Build Failed"
			}
		}
}
