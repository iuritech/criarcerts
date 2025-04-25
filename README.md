# guia

    su
    cd

1-

    bash ciber/1criarcert.ssh  

2-

    vi /root/ca/intermediate/openssl.cnf

#macros pesquisar yy

    crt+r
    "

3- #Adicionar server sert e alterar os campos 

    server_cert
    subjectAltName = @alt_names
    [alt_names]
    DNS.1 = www.simoes.com

    dir 		  = /root/ca/intermediate
    private_key 	  = $dir/private/intermediate.key.pem
    certificate 	  = $dir/certs/intermediate.cert.pem
    crl 	 	  = $dir/crl/intermediate.crl.pem
    policy 	  	  = policy_loose

4-

    bash ciber/2criarcert.ssh  

    comon = www.simoes.com
    email = iuri.nunes@ipcbcampus.pt
