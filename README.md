# guia

1- entrar em super user na pasta /root

    su
    cd

2- criar certificados "Autoridade Raiz"

mail= iuri.nunes@ipcbcampus.pt

    bash ciber/1criarcert.ssh  

3- Adicionar server sert e alterar os campos 

    vi /root/ca/intermediate/openssl.cnf

#macros pesquisar yy

    crt+r
    "

    server_cert
    subjectAltName = @alt_names
    [alt_names]
    DNS.1 = www.simoes.com

    dir 		  = /root/ca/intermediate
    private_key 	  = $dir/private/intermediate.key.pem
    certificate 	  = $dir/certs/intermediate.cert.pem
    crl 	 	  = $dir/crl/intermediate.crl.pem
    policy 	  	  = policy_loose

5- Criar cert "Autoridade Intermedia" e cert server "www.simoes.com"

    bash ciber/2criarcert.ssh  

    comon = www.simoes.com
    email = iuri.nunes@ipcbcampus.pt
