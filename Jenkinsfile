node {
    stage("Checkout") {
        checkout scm
    }
    stage("Build") {
        sh "mvn -DskipTests=true clean verify"
    }
}
stage("Test") {
    parallel (
        "Firefox" : { sleep 7 },
        "Edge" : { sleep 9 }
    )    
}
stage("Deploy") {
    sleep 5
} 
