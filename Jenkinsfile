node{
   stage('SCM Checkout'){
     
     git 'https://github.com/AshishBang/Sample-Maven-App.git'
   }
   stage('Compile Package'){
      // Get maven home path
      def mvnHome = tool name: 'maven3', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
      // Send email 
      mail bcc: '', body: '''Hi Welcome to Jenkins email alerts
      Thanks
      Ashish''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'bangashish@gmail.com'
   }
}
     
    
