node {
  checkout scm
  def dockerfile = './dockerfiles/Dockerfile.test'
  def customImage = docker.build("my-image:${env.BUILD_ID}", "-f ${dockerfile} ./dockerfiles")
}
