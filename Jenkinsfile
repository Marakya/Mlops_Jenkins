pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    
    stage('run') {
        steps {
            build job : "requirements.txt"
        }
    }
    
//     stage('install scikit-learn') {
//         steps {
//             sh 'python3 -m pip install scikit-learn'
//             echo 'scikit-learn'
//         }
//     }
    
//     stage('install numpy') {
//         steps {
//             sh 'python3 -m pip install numpy'
//             echo 'numpy'
//         }
//     }
    
//     stage('install pandas') {
//         steps {
//             sh 'python3 -m pip install pandas'
//             echo 'pandas'
//         }
//     }
    
//     stage('install scipy') {
//         steps {
//             sh 'python3 -m pip install scipy'
//             echo 'scipy'
//         }
//     }
    
    stage('data creation') {
      steps {
        sh 'python3 data_creation.py'
        echo 'Create data'
      }
    }
    
    stage('data_preprocessing') {
      steps {
        sh 'python3 model_preprocessing.py'
        echo 'Data preprocessing'
      }
    }
    
    stage('data_preparation') {
      steps {
        sh 'python3 model_preparation.py'
        echo 'Data training'
      }
    }
    
    stage('model_testing') {
      steps {
        echo 'Prediction'
        sh 'python3 model_testing.py'
      }
    }
  }
}
