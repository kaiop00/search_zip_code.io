pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Teste de conexÃ£o jenkins'
        sleep(time: 10, unit: 'SECONDS')
      }
    }

    stage('teste') {
      steps {
        echo 'iniciando teste'
        sleep(time: 10, unit: 'SECONDS')
        build(job: 'teste_unitario', propagate: true)
      }
    }

    stage('deploy') {
      steps {
        mail(to: 'kaioportela10@gmail.com', subject: 'teste de conexão', body: 'Realizando um teste para saber se está tudo ok!!!')
      }
    }

  }
}