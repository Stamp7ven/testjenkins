pipeline {
    agent { label 'window-agent'} // This means the pipeline can run on any available agent

    stages {
        stage('Hello') {
            steps {
                echo 'Hello, Jenkins!' // A simple command to print a message
            }
        }

        stage('Check Docker Connectivity') {
            steps {
                echo 'Checking Docker installation and connectivity...'
                // รันคำสั่ง docker version เพื่อดูเวอร์ชันของ Docker
                // และตรวจสอบว่า Docker daemon กำลังทำงานอยู่หรือไม่
                sh 'docker version'
                // หรือ
                // sh 'docker info' // จะให้ข้อมูลรายละเอียดเพิ่มเติมเกี่ยวกับ Docker daemon
            }
        }
        
        stage('Run a simple Docker container') {
            steps {
                echo 'Running a simple "hello-world" Docker container...'
                // ดึงและรัน image 'hello-world' ซึ่งเป็น image เล็กๆ สำหรับทดสอบ
                // --rm จะลบ container ออกไปทันทีหลังจากรันเสร็จ
                sh 'docker run --rm hello-world'
            }
        }
    }
}
