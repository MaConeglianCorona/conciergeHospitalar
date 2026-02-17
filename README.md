# conciergeHospitalar
Plataforma web integrada a um dispositivo IoT (ESP32) para gerenciamento de solicitações hospitalares.


[LINK DA ARQUITETURA PROVAVEL (V1):](https://www.tldraw.com/f/jtJjZGkqKzSB5w92QAjFr?d=v-446.-500.2808.1605.page) 

***************************************************************************************************************
Ferramentas que serao usadas:
IOT  
  BOTAO|LED|ESP32

BACKEND
  PHP 8+
  Laravel
  PostgreSQL

FRONTEND
  Vue.js
  Quasar Framework
***************************************************************************************************************
Formato json

Chamada de Enfermagem (ESP32)
POST /api/chamadas
{
  "cd_leito": 10,
  "tipo": "CHAMADA_ENFERMAGEM"
}
=====================================================
Cadastro de Itens da Cozinha (feito pela cozinha)
POST /api/itens-cozinha

{
  "nome": "Água",
  "descricao": "Copo 200ml",
  "ativo": true
}
=====================================================
Paciente realiza pedido
POST /api/solicitacoes

{
  "cd_paciente": 55,
  "cd_item": 3,
  "tipo": "COZINHA"
}
=====================================================
Atualização de Status (Cozinha)
PUT /api/solicitacoes/102/status

{
  "status": "EXECUTANDO"
}
=====================================================
Registro de Sintoma
POST /api/sintomas

{
  "cd_paciente": 55,
  "tipo": "DOR",
  "intensidade": 7,
  "descricao": "Dor abdominal"
}
***************************************************************************************************************
DB: PostgreSQL.
Tecnologia/Linguagem da API: PHP, Laravel, REST API, Comunicaçao via HTTP + JSON
Plataforma de Prototipagem: Wokwi




