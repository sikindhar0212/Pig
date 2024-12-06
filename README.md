# Pig
configure PIG

wget https://dlcdn.apache.org/pig/pig-0.17.0/pig-0.17.0.tar.gz
tar -xvf pig-0.17.0.tar.gz
mv pig-0.17.0/ /opt/pig

#Set up PIG profile
export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64/jre
export PIG_HOME=/opt/pig
export PATH=$PATH:$PIG_HOME/bin
export PIG_CLASSPATH=$HADOOP_HOME/conf


#we can change in .bashrc instead of exporting the path variables every time
#instead of changing at .bashrc we create script under profile.d (while doing in your own VM)
#sudo tee /etc/profile.d/pig.sh <<'EOF'
#export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64/jre
#export PIG_HOME=/opt/pig
#export PATH=$PATH:$PIG_HOME/bin
#export PIG_CLASSPATH=$HADOOP_HOME/conf
#EOF

#Set up PIG profile(for script we need like below)
#cat >/etc/profile.d/pig.sh <<'EOF'
#export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64/jre
#export PIG_HOME=/opt/pig
#export PATH=$PATH:$PIG_HOME/bin
#export PIG_CLASSPATH=$HADOOP_HOME/conf
#EOF
