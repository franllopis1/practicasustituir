pipeline {
  agent any
  stages {
    stage('practica') {
      steps {
        //IFS=$'\n' es necesario para que no conte por palabras
        sh '''
        IFS=$'\n' 
        for i in `cat release.yaml`
        do
          echo "La version `echo "$i" | cut -d ":" -f1` es`echo "$i" | cut -d ":" -f2`"
        done
        '''
      }
    }
  }
}