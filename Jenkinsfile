pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Teste de conex√£o jenkins'
        sleep(time: 10, unit: 'SECONDS')
      }
    }

    stage('teste') {
      steps {
        echo 'iniciando teste'
        sleep(time: 10, unit: 'MINUTES')
        build(job: 'free-style', propagate: true)
      }
    }

    stage('deploy') {
      steps {
        mail(to: 'kaioportela10@gmail.com', subject: 'teste de conex„o', body: 'Realizando um teste para saber se est· tudo ok!!!')
      }
    }

  }
}