AWAKENING SYSTEM v0.1

Conteúdo:
- index.html: app web funcional, mobile-first
- manifest.json: configuração de instalação PWA
- sw.js: cache offline básico

Funcionalidades nesta versão:
- interface inspirada em RPG de evolução pessoal
- XP, níveis e seis atributos
- missões diárias, conclusão e histórico
- foco e tempo diário configuráveis
- salvamento local no navegador
- exportação de progresso em JSON
- layout responsivo para iPhone

Limitações importantes:
- O motor de missões é baseado em regras nesta primeira versão, não em IA.
- Ainda não existe login, sincronização, notificações push ou backend.
- Para usar como app instalável com funcionamento PWA, publique estes arquivos em um host HTTPS (por exemplo, GitHub Pages). Depois abra a URL no Safari e use Compartilhar > Adicionar à Tela de Início.
- A IA real deve ser conectada por um backend seguro, nunca colocando uma chave secreta de API dentro do HTML público.
- Os dados desta versão ficam no armazenamento local do navegador. Exporte o progresso periodicamente.

Próxima etapa de arquitetura:
iPhone/PWA -> backend seguro -> modelo de IA
O backend enviará ao modelo somente o perfil e o histórico necessários, validará as missões retornadas e calculará XP/níveis com regras determinísticas. A IA sugere/adapta missões; o código controla progressão e integridade dos dados.
