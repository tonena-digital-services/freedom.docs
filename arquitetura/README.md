##### Brainstorm
Se Freedom pode ter mais que 100k de usuários simultaneos, então a comunicação entre 100k dispositivos clientes deve ser eficaz e eficiente.

Proposta de mecanismo pra troca de msgs: gRPC.
Aceito proposta: gRPC pra gerenciar a troca de pacotes de msgs.

Mas isso não significa um protocolo, apenas o mecanismo de troca de msgs.

---

-Persistir as mensagens trocadas? Qual o proposito de se gravar as mensagens trocadas? contexto: backend + frontend devem estar online/tempo real, portanto se qualquer um dos dois cair, a sessão se perde, e deve-se reiniciar. 

!!Feature!!: Se backend cair e tudo estiver gravado, frontend não perde nada. Se frontend cair e backend estiver bem, então frontend apenas retorna e tudo bem. 

---

Segurança: Como tudo será efemero (MVP), então não há motivo pra criptografar dados gravados, apenas canal seguro TLS/SSL.

---

Sessão: O concorrente usa sessão anonima, ninguem precisa ter conta, ou se logar, apenas escolher um nick para ser utilizado na sala desejada.

---

Framework:backend: Quarkus (java)

---

Framework:frontend: Flutter (dart)

---

##### Definições Arquiteturais:

---

-Troca de mensagens: gRPC;
-Sem gravar/persistir sessão do usuário (MVP);
-Sessão anonima;
-Framework:backend: Quarkus (java)
-Framework:frontend: Flutter (dart)

---

Glossário:

-Eficaz: Que funciona.
-Eficiência: Que funciona bem.
-Sessão: Quando o usuário ENTRA NUMA SALA, uma SESSÃO EFÊMERA é criada. Efêmera no sentido de que a SESSÃO PERDURA ATÉ O USUÁRIO SAIR DA SALA.

