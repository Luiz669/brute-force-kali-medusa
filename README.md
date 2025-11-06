# brute-force-kali-medusa
simulação de ataques de força bruta com Kali Linux e Medusa
________________________________________
# 🔐 Simulação de Ataques de Força Bruta com Kali Linux e Medusa

Este projeto foi desenvolvido como parte do desafio da DIO para aplicar conhecimentos em segurança ofensiva. Utilizando Kali Linux, Medusa e ambientes vulneráveis como Metasploitable 2 e DVWA, foram simulados ataques de força bruta em serviços FTP, Web e SMB, com foco em aprendizado, documentação e mitigação.

## 🧠 Objetivos de Aprendizagem

- Compreender ataques de força bruta em diferentes serviços (FTP, Web, SMB)
- Utilizar Kali Linux e Medusa para auditoria de segurança em ambiente controlado
- Documentar processos técnicos de forma clara e estruturada
- Reconhecer vulnerabilidades comuns e propor medidas de mitigação
- Utilizar o GitHub como portfólio técnico para compartilhar evidências

## 🛠️ Tecnologias e Ferramentas Utilizadas

- Kali Linux (VM)
- Metasploitable 2 (VM)
- DVWA (Damn Vulnerable Web Application)
- Medusa
- Nmap
- VirtualBox (rede interna host-only)
- Wordlists personalizadas

## ⚙️ Configuração do Ambiente

1. Criar duas VMs no VirtualBox:
   - Kali Linux
   - Metasploitable 2
2. Configurar rede interna (host-only) entre as VMs
3. Verificar conectividade com `ping` e `nmap`

## 🚨 Cenários de Ataque Simulados

### 1. Ataque de Força Bruta em FTP

- Serviço alvo: vsftpd no Metasploitable 2
- Comando utilizado:
  ```bash
  medusa -h 192.168.56.101 -u admin -P wordlist.txt -M ftp
•	Resultado: acesso obtido com credencial fraca
•	Mitigação: desabilitar FTP, usar SFTP, aplicar políticas de senha
2. Automação de Tentativas em Formulário Web (DVWA)
•	Nível de segurança: baixo
•	Script em Python com requests para automação
•	Wordlist simples com senhas comuns
•	Resultado: acesso ao painel DVWA
•	Mitigação: limitar tentativas, usar CAPTCHA, autenticação multifator
3. Password Spraying em SMB com Enumeração de Usuários
•	Enumeração com enum4linux
•	Ataque com Medusa: 
•	medusa -h 192.168.56.101 -U users.txt -P passlist.txt -M smbnt
•	Resultado: acesso obtido com senha padrão
•	Mitigação: bloquear contas após tentativas, monitorar logs, aplicar senhas fortes
📁 Estrutura do Repositório
├── README.md
├── wordlists/
│   ├── wordlist.txt
│   ├── users.txt
│   └── passlist.txt
├── scripts/
│   └── dvwa_bruteforce.py
├── images/
│   ├── ftp_attack.png
│   ├── dvwa_login.png
│   └── smb_enum.png
🧾 Recomendações de Mitigação
•	Implementar autenticação multifator
•	Monitorar logs de acesso e falhas
•	Utilizar senhas fortes e únicas
•	Limitar tentativas de login por IP
•	Desabilitar serviços inseguros
👨‍💻 Autor
Luiz Augusto S. Santos
Projeto realizado em novembro de 2025 como parte da formação em segurança ofensiva na DIO.
________________________________________

