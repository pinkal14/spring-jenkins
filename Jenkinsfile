pipeline
{
  agent any
  
  
   tools { 
        maven 'Maven 4.0.0' 
        jdk 'jdk8' 
    }
  
   stages {
   
   stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }
   
    
        stage('Build') { 
            steps { 
               echo 'This is a minimal pipeline.' 
            }
        
    }
    
      stage('Compile Stage')
      {
         steps {
             withMaven(maven : 'maven_4_0_0') {
               sh 'mvn clean compile'
             } 
         }
      }
      
      stage('Testing Stage')
      {
         steps {
             withMaven(maven : 'maven_4_0_0') {
               sh 'mvn test'
             } 
         }
      }
      
      stage('Deployment Stage')
      {
         steps {
             withMaven(maven : 'maven_4_0_0') {
               sh 'mvn deploy'
             } 
         }
      }
    
    
   }

}

