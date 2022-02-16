# GreenGrok

How make the server part : 

- Many arguments are mandatory :
    - --clean allow to use the configuration by argument rather than config file
    - --isfrontend this argument announces that the script will be used in server mode
    - --protos define the prototypes authorized by the server
    - --domain it's most import argument first part define the speficics prototype use by this ip adress or DNS the second part is the IP or DNS and the last is the password use to connect the client at this tunnel in the server
    - --ports this argument corresponds to ports listen by the server

Exemple :
    python GreenGrok.py --clean --isfrontend --protos=http,https --domain=http,https:nameofyourdns:password --ports=80,443"

How make the client part : 

- Many arguments are mandatory :
    - --clean allow to use the configuration by argument rather than config file
    - --frontend search to trigger your server part so part one corresponding to your DNS name and the second part correspond to the port listening by your server
    - --service this argument corresponds to the creation of the tunnel, first part is the protocol, the second the DNS, the third is the localhost you want to expose and the last is the port your localhost is on
    - --ports this argument corresponds to the ports of our server that we are trying to reach


Exemple :
    python GreenGrok.py --clean --ports=listeningport(80) --frontend=nameofyourdns:listeningport(80) --service_on=http:nameofyourdns:localhost:6666:password
