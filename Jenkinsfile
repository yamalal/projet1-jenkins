pipeline{
  agent any

  tools {
    nodejs 'node20-11'
  }
//   environment {
//     SERVER_USER = 'root'
//     SERVER_IP = '192.168.15.89'
//   }
 stages 
 {
    stage('check') {
        steps {
          sh 'node -v'
          sh 'npm -v'
        }
    }

 }
//   stages {
//     stage('Installer les dependences'){
//       steps {
//         dir('server') {
//             sh 'npm ci --cache .npm --prefer-offline'
//         }
//         }
//     }
//     stage('Execute les tests') {
//       steps {
//         dir('server') {
//           sh 'npm run test:ci'
//             }
//         }
//     }
//     stage('Vérifier le code') {
//       steps {
//         dir('server') {
//           sh 'npm run lint'  
//         }
//       }  
//     }
//     stage('Vérifier les depndances') {
//       steps {
//         dir('server') {
//           sh 'npm audit'  
//         }
//       }  
//     }
//     // stage('Deployer sur le serveur') {
//     //   steps {
    
//     //       sshagent(credentials: ['ovh_prod_key']) {
//     //         sh '''
//     //           [ -d ~/.ssh ] || mkdir ~/.ssh && chmod 0700 ~/.ssh
//     //           ssh-keyscan -H $SERVER_IP >> ~/.ssh/known_hosts
//     //           rm -rf ./server/node_modules
//     //           scp -r ./server $SERVER_USER@$SERVER_IP:/var/www
//     //           ssh $SERVER_USER@$SERVER_IP "cd /var/www/server && npm install --omit=dev"
//     //           ssh $SERVER_USER@$SERVER_IP "cd /var/www/server && pm2 startOrRestart ecosystem.config.js --env production && pm2 save"
//     //          '''
//     //     }
//     //   }  
//     // }
//   }
  
} 
