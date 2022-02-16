# GreenGrok

How make the server part : 

- Many arguments are mandatory :
    - --clean allow to use the configuration by argument rather than config file
    - --isfrontend this argument announces that the script will be used in server mode
    - --protos=http,https define the prototypes authorized by the server
    - --domain=http,https:82.64.95.42:gpk it's most import argument first part define the speficics prototype use by this ip adress or DNS the second part is the IP or DNS and the last is the password use to connect the client at this tunnel in the server
    - --ports=80,443 this argument corresponds to 

Exemple :
    python GreenGrok.py --clean --isfrontend --protos=http,https --domain=http,https:nameofyourdns:password --ports=80,443"

How make the client part : 

- Many arguments are mandatory :
    - --clean allow to use the configuration by argument rather than config file
    - --frontend search to trigger your server part so part one corresponding to your DNS name and the second part correspond to the port listening by your server
    - --service=http,https:82.64.95.42:gpk this argument corresponds to the creation of the tunnel, first part is the protocol, the second the DNS, the third is the localhost you want to expose and the last is the port your localhost is on.


Exemple :
    python GreenGrok.py --clean --frontend=nameofyourdns:listeningport(80) --service_on=http:nameofyourdns:localhost:6666:password
