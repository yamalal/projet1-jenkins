pipeline {
    agent any

    environment {
        NODEJS_HOME = tool name: 'Node 6.x', type: 'NodeJSInstallation'
        PATH = "${NODEJS_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Setup') {
            steps {
                script {
                    // Vérifiez que Node.js est bien installé
                    sh 'node -v'
                    sh 'npm -v'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    // Ajoutez vos étapes de build ici
                    sh 'npm install'
                    sh 'npm run build'
                }
            }
        }
    }
}

// pipeline{
//   agent any
 
//   tools { 
//     nodejs 'node20-11'
//   }
// //   environment {
// //     SERVER_USER = 'root'
// //     SERVER_IP = '192.168.15.89'
// //   }
 
//  stages {
//     stage('Check backend'){
//       steps {
//         dir('server') {
//           sh 'npm ci --cache .npm --prefer-offline'
//           sh 'npm run test:ci'
//           sh 'npm run lint'
//           sh 'npm audit'  
//         }
//         }
//       post {
//         always {
//           withCredentials([string(credentialsId: 'CODECOV', variable: 'CODECOV_TOKEN')]) {
//             dir('server') {
//               sh "/home/jenkins/codecov -t ${CODECOV_TOKEN}"
//           }
//         }
//        }
//       }   
//     }
//     stage('Check frontend'){
//       steps {
//         dir('client') {
//           sh 'npm ci --cache .npm --prefer-offline'
//           sh 'npm run lint'
//           sh 'npm audit'  
//         }
//       }
//     }

//     stage('Build frontend'){
//       steps {
//         dir('client') {
//           sh 'npm run build' 
//         }
//       }
//     }
//     stage('Test e2e'){
//       steps {
//         dir('server') {
//           sh 'node index.js &' 
//         }
//         dir('client') {
//           sh 'NO_COLOR=1 npm run test:e2e' 
//         }
//       }
//     }

//     // stage('Couverture codecov') {
//     //   steps {
//     //     withCredentials([string(credentialsId: 'CODECOV', variable: 'CODECOV_TOKEN')]) {
//     //       dir('server') {
//     //         sh "/home/jenkins/codecov -t ${CODECOV_TOKEN}"
//     //       }
//     //     }
//     //   }  
//     // }
//     // stage('Deployer sur le serveur') {
//     //   steps {
    
//     //       sshagent(credentials: ['ovh_prod_key']) {
//     //         sh '''
//     //           [ -d ~/.ssh ] || mkdir ~/.ssh && chmod 0700 ~/.ssh
//     //           ssh-keyscan -H $SERVER_IP >> ~/.ssh/known_hosts
//     //           rm -rf ./server/node_modules
//     //           scp -r ./server $SERVER_USER@$SERVER_IP:/var/www
//     //           scp -r ./client/dist $SERVER_USER@$SERVER_IP:/var/www
//     //           ssh $SERVER_USER@$SERVER_IP "cd /var/www/server && npm install --omit=dev"
//     //           ssh $SERVER_USER@$SERVER_IP "cd /var/www/server && pm2 startOrRestart ecosystem.config.js --env production && pm2 save"
//     //          '''
//     //     }
//     //   }  
//     // }
//   }
  
// } 
