pipeline {
    agent any
    parameters
    {
        string(name: 'ip', defaultValue: '192.168.56.200', description: 'IPcim')
    }
    stages {
        stage('Install')
        {
            steps            {
                sh 'yum install -y https://download.postgresql.org/pub/repos/yum/10/redhat/rhel-7-x86_64/pgdg-redhat10-10-2.noarch.rpm'
            }
        }
        stage('Dump') 
        {
        
            steps {
                sh '''
                export PGPASSWORD="000000"
                     pg_dump -h ${ip} -U postgres -d postgres -C >> postgreDump999.sql
                '''
                
                
            }
        }
    }
}
