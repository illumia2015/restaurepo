node {
    stage('preparation') {
        // Checkout the master branch of the Laravel framework repository
        git branch: 'dev', url: 'https://github.com/illumia2015/restaurepo.git'
    }
    stage("composer_install") {
        // Run `composer update` as a shell script
        sh 'composer install'
    }    

    stage("phpunit") {
        // Run PHPUnit
        sh 'cd application/tests/'
        sh 'vendor/bin/phpunit'
    }
}
