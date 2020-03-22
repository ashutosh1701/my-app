
node {
   def mvn = tool (name: 'mavendefault', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    // Clone repo
	git branch: 'master', 
	credentialsId: 'github', 
	url: 'https://github.com/ashutosh1701/my-app' 
   }
    	
   stage('Mvn Package'){
	   // Build using maven	   
	   sh "${mvn} clean test package"
   }
   
}
