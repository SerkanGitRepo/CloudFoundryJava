@Library('piper-lib-os') _
node() {
	stage('prepare') {
		checkout scm
		setupCommonPipelineEnvironment script:this
	}
	stage('build') {
		mtaBuild script: this
	}
	
	stage('security'){
		whitesourceExecuteScan: this
	}
	
//	stage('deploy') {
//		cloudFoundryDeploy script: this
//	}
}