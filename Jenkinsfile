node {

	stage('Build'){
		sh 'echo "New Build stage"'
		stage('Build a'){
			sh 'echo "Build stage"'
		}
	}

	stage('API Integration Tests') {
		parallel Database1APIIntegrationTestParallel: {
			 stage ('Database1 API Integration Test'){
				try {
							   
					sh 'echo "stage1 in Database1APIIntegrationTest"'
				}
				finally {
					sh 'echo "Finished stage1 in Database1APIIntegrationTest"'
				}               
			}

			stage ('stage2 in Database1 API Integration Test'){
				try {
					sh 'echo "stage2 in Database1 API Integration Test"'
				}
				finally {
					sh 'echo "Finished stage2 in Database1 API Integration Test"'
				}               
			}
		}, Database2APIIntegrationTestParallel: {
			
			stage ('stage1'){
				try {   
					sh 'echo "stage1 in Database2APIIntegrationTest"'
				}
				finally {
					sh 'echo "Finished stage1 in Database2APIIntegrationTest"'
				}  

				stage ('stage1a in Database2APIIntegrationTest'){
							       
				}	
				stage ('stage1b in Database2APIIntegrationTest'){
							       
				}					
			}

			stage ('stage2'){
				try {
					sh 'echo "stage2 in Database2APIIntegrationTest"'
				}
				finally {
					sh 'echo "Finished stage2 in Database2APIIntegrationTest"'
				}               
			}  
			stage ('stage3'){
				try {
					sh 'echo "stage2 in Database2APIIntegrationTest"'
				}
				finally {
					sh 'echo "Finished stage2 in Database2APIIntegrationTest"'
				}               
			}  			
		}
		
	}

	stage('System Tests') {
		sh 'echo "In System Tests"'
	}
}
