FROM jenkins/jenkins:lts

COPY --chown=jenkins:jenkins plugins_extra.txt /usr/share/jenkins/ref/plugins_extra.txt

ENV JENKINS_HOME /var/jenkins_home

ARG JAVA_OPTS
ENV JAVA_OPTS "-Djenkins.install.runSetupWizard=false ${JAVA_OPTS:-}"

RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins_extra.txt

