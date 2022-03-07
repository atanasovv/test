#!groovy
node  {
    stage ('build') {

        sh("./build.sh 2>&1 | tee /dev/tty | gzip --stdout > build.log.gz")

        archiveArtifacts(allowEmptyArchive: true, artifacts: '*.log.gz', followSymlinks: false) 

    }
}