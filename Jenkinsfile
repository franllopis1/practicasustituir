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
          echo "La version `echo "$i" | cut -d ":" -f1` antes`echo "$i" | cut -d ":" -f2` ahora es`echo "$i" | cut -d ":" -f2 | sed -i 's/0.0/1.0/g' release.yaml`"
        done
        '''
      }
    }
  }
}