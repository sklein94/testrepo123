#!groovy
@Library('github.com/cloudogu/ces-build-lib@1.35.1')
import com.cloudogu.ces.cesbuildlib.*

properties([
        // Don't run concurrent builds, because the ITs use the same port causing random failures on concurrent builds.
        disableConcurrentBuilds()
])

node {

    stage('Checkout') {
        checkout scm
    }

    stage("archive") {
        archiveArtifacts "test.html"
    }

}
