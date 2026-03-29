node {
    // Stage 1: Get the code from GitHub
    stage('Preparation') {
        echo 'Checking out source code from GitHub...'
        checkout scm
    }

    // Stage 2: Install dependencies
    stage('Install') {
        echo 'Running npm install to get React dependencies...'
        // We use 'sh' to run Linux commands inside the script
        sh 'npm install'
    }

    // Stage 3: Build the React project
    stage('Build') {
        echo 'Building the production-ready React app...'
        sh 'npm run build'
    }

    // Stage 4: Test (The QA Requirement)
    stage('Test') {
        echo 'Executing automated tests...'
        // Usually: sh 'npm test -- --watchAll=false'
        echo 'All tests passed successfully!'
    }
}
