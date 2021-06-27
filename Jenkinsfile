pipeline
{
  agent any
  
  
    
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



