# BypassDeautentica-oOpenSSH
O OpenSSH lançou a versão 10.6p2 corrigindo uma falha crítica de bypass de autenticação em sistemas com musl libc (como Alpine) sem PAM. Contas de chave única aceitavam qualquer senha longa. Mitigação: atualize o OpenSSH ou desative o `PasswordAuthentication`.
