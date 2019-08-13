pipeline {
    agent any

    stages {   
        stage('py2_real_build') {
            steps {
                sh 'cp config.mk.info config.mk'
                sh '. $HOME/packages/setMdolabPath; conda activate py2; env|sort; make'
            }
        }

        /* No tests available
        stage('py2_real_test') {
            steps {
                sh '. $HOME/packages/setMdolabPath; conda activate py2; env|sort; cd python/reg_tests; python run_reg_tests.py -nodiff'
            }
        }
        */
    }
}