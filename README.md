# Prospect CRM

CRM em português para prospecção de clientes de sites. Uso individual, sem backend e sem cadastro adicional. Os dados são armazenados em `localStorage` no navegador e não são sincronizados entre dispositivos. Use **Baixar backup** regularmente; limpar os dados do navegador apaga a base local.

## Executar

Com Node.js instalado, execute `npm start` e abra http://127.0.0.1:4173. Os arquivos em `dist/` também podem ser publicados em qualquer hospedagem estática HTTPS. Execute `npm test` para verificar normalização, deduplicação e links.

## Funcionalidades

- Importação XLSX, XLS e CSV, seleção de aba, mapeamento de colunas, prévia e descarte de duplicados por nome, cidade e telefone.
- Lista com busca, filtros de bairro e etapa, ordenação por avaliações, nota, nome ou retorno.
- Atalhos para Google Maps, Instagram e WhatsApp. Os links abrem o aplicativo/site; mensagens não são enviadas automaticamente.
- Funil com seis etapas, cadastro manual, edição, exclusão, anotações e agenda de retorno.
- Exportação CSV dos resultados filtrados e backup/restauração JSON de toda a base.
- Layout responsivo, controles acessíveis e estados vazios.

Limites: 10 MB por planilha e 20.000 linhas por importação. Sem autenticação própria, integração de mensagens, validação de existência de WhatsApp ou sincronização na nuvem. O armazenamento disponível depende do navegador. Exportar CSV é para consulta; use JSON para restaurar etapas, anotações e datas.

O repositório inicia com base vazia e não inclui contatos. Importe sua própria planilha pelo aplicativo. Perfis de Instagram ausentes não são inferidos.

Planilhas são tratadas apenas como dados, sem execução de fórmulas ou instruções. Biblioteca SheetJS CE 0.20.3 vendorizada de https://cdn.sheetjs.com/xlsx-0.20.3/package/dist/xlsx.full.min.js (Apache-2.0); fontes DM Sans e Manrope via Google Fonts (a interface usa fonte local de fallback sem conexão).
