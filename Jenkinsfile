node {
   def mvnHome
   stage('Checkout') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/srikns/SampleJenkinsPipelineProject.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      mvnHome = tool 'M2'
   }
   stage('Build') {
      echo "Build"
   }
    stage('Blazemeter Test') {
      echo "Blazemeter Test"
   }
   stage('CA APM Plugin') {
      echo "CA APM Plugin"
   }
   stage ('Mail Notification') {
       echo "Mail Notification"
       
       mail to: "srikns@yahoo.com",
       body: "Something Went Wrong in the Build",
       subject: "Jenkins ${currentBuild.fullDisplayName}"
   }
}
