#!/usr/bin/env/ groovy 

import hudson.model.*
import hudson.EnvVars
import java.net.URL

node{
    stage('Git Checkout'){
      git 'https://github.com/wintahailai8/code.git'  
    }
    stage('compile') {
        withMaven(maven:'my maven') {
        sh 'mvn compile'
        }
    }
    stage('package'){
        withMaven(maven:'my maven'){
        sh 'mvn package'
        }
    }
}

