#!groovy
node {
    stage("build"){

        sh("./build.sh 2>&1 | tee >(gzip > build.log.gz)")

        archiveArtifacts(allowEmptyArchive: true, artifacts: '*.log.gz', followSymlinks: false) 

    }
}