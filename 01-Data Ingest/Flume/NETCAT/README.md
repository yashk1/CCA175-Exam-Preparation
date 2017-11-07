
# Nombrar los componentes del agente
agent1.sources = netcat1
agent1.channels = memory1
agent1.sinks = hdfs1

# Configuracion del source
agent1.sources.netcat1.type = netcat
agent1.sources.netcat1.bind = localhost
agent1.sources.netcat1.port = 9999

# Configuracion del channel
agent1.channels.memory1.type = memory

# Configuracion del sink
agent1.sinks.hdfs1.type = hdfs 
agent1.sinks.hdfs1.hdfs.path = /tmp/flume-netcat-to-hdfs-test1

# Unir el source y el sink al channel
agent1.sources.netcat1.channels = memory1
agent11.sinks.hdfs1.channel = memory1