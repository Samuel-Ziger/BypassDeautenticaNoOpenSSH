Bypass de autenticação no OpenSSH!

OpenSSH lançou às pressas uma atualização para uma falha crítica que permite que atacantes façam login em alguns servidores Linux sem a senha correta.

Uma falha crítica no OpenSSH poderia permitir que atacantes remotos burlassem a autenticação por senha em servidores Alpine Linux afetados, incluindo contas destinadas a acesso somente por chave. 
O OpenSSH lançou a versão Portable 10.6p2 em 5 de novembro de 2026 para corrigir o problema, que afeta sistemas Linux que utilizam a biblioteca musl libc sem autenticação PAM.

Basicamente em contas com * em /etc/shadow (usuários apenas com chave, root em imagens de nuvem Alpine, etc.) aceitam qualquer senha com mais de 256 caracteres quando o sshd é compilado sem PAM.

Mitigação sem o update: Desative PasswordAuthentication.

A versão 10.6p2 contorna o problema. Sistemas no glibc ou PAM não são afetados.

Fonte: https://www.openssh.org/txt/release-10.6p2
