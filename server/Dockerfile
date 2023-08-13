# 이미지 설정
FROM openjdk:17-jdk
# 포트설정
EXPOSE 8080
# 빌드된 jar 파일 위치를 변수로 설정
ARG JAR_FILE=/var/jenkins_home/workspace/majjeom/server/build/libs/*.jar
# jar 파일을 컨테이너 내부에 복사하고 권한 설정
COPY --chown=1000:1000 ${JAR_FILE} server.jar
# 실행 명령어
ENTRYPOINT ["java","-jar","server.jar"]