# Revisor Inteligente de Matriz Curricular — Kickoff de Produto (v1)

## Objetivo
Transformar o processo de revisão curricular em um fluxo padronizado, rastreável e orientado por evidências, cruzando:
1. Planilha de revisão da instituição
2. DCNs do curso
3. Matrizes de referência ENADE (por curso/ciclo)
4. Ementas e materiais acadêmicos

---

## Fase 1 — Descoberta (perguntas-chave)

### 1) Problema e sucesso
- Qual curso vamos priorizar no lançamento (ex.: Administração, Direito, Enfermagem)?
- Qual ciclo ENADE é prioridade imediata?
- Como você vai medir sucesso em 60 dias?
  - redução do tempo de revisão?
  - redução de lacunas?
  - melhor documentação para regulação?

### 2) Entradas e dados
- Em qual formato está sua planilha de revisão (Google Sheets, Excel, ambos)?
- As ementas e bibliografias estão em PDF, DOCX, planilhas, links de Drive?
- As DCNs e matrizes ENADE serão enviadas manualmente ou puxadas de uma base já curada?
- Você precisa suportar múltiplas IES desde o início, ou começamos em uma só?

### 3) Saídas esperadas
- Quais decisões você precisa tomar com o relatório?
  - ajustar carga horária?
  - criar/remodelar disciplinas?
  - justificar aderência em auditorias?
- Qual formato mínimo de entrega é obrigatório na v1?
  - dashboard web
  - planilha preenchida automaticamente
  - relatório PDF com evidências

### 4) Operação e governança
- Quem valida o diagnóstico final (coordenação, NDE, regulação)?
- Existe política de aprovação por etapa?
- Quais restrições de LGPD e segurança são inegociáveis?

---

## Fase 2 — Planejamento (escopo v1)

## v1 (must-have)
1. Upload guiado de documentos (DCN, ENADE, ementas e planilha)
2. Extração de texto e indexação por documento/trecho
3. Mapeamento inicial disciplina ↔ competência/tema
4. Diagnóstico com 3 status por item:
   - coberto
   - parcialmente coberto
   - não coberto
5. Evidências rastreáveis (trecho da ementa + referência DCN/ENADE)
6. Exportação para planilha e relatório executivo

## v1.1+ (depois)
- Recomendações automáticas de reformulação de ementa
- Comparação de evolução entre ciclos ENADE
- Benchmark entre cursos/IES
- Workflow de aprovação multiusuário

## Abordagem técnica (linguagem simples)
- Um pipeline lê os arquivos, limpa os textos e separa por blocos.
- Esses blocos são comparados com critérios da DCN e ENADE.
- O sistema calcula aderência e aponta lacunas com justificativas.
- A interface mostra o diagnóstico e permite exportar tudo para uso institucional.

## Complexidade estimada
- v1: **média** (resultado real e demonstrável em semanas)
- v2 multi-IES com governança forte: **ambiciosa**

---

## Fase 3 — Construção (entregas em estágios)

1. **Marco A — Ingestão de documentos**
   - validar formatos e pipeline de leitura
2. **Marco B — Mapeamento e aderência**
   - primeira versão do motor de comparação
3. **Marco C — Evidências e lacunas**
   - rastreabilidade completa por trecho
4. **Marco D — Exportações e usabilidade**
   - planilha final e relatório executivo

Cada marco precisa de:
- demonstração
- testes mínimos
- decisão do dono do produto antes de avançar

---

## Fase 4 — Polimento
- Mensagens de erro claras (arquivo inválido, texto ilegível, duplicidade)
- Padronização de nomenclaturas
- Garantia de desempenho para lotes médios de disciplinas
- Visual profissional para compartilhamento com stakeholders

---

## Fase 5 — Entrega
- Deploy em ambiente acessível para o time
- Manual curto de operação
- Guia de manutenção e evolução
- Lista objetiva de melhorias da v2

---

## Decisões de Produto (para destravar agora)
1. Curso piloto da v1
2. Ciclo ENADE inicial
3. Formato oficial da planilha de revisão
4. Nível de automação esperado na primeira entrega
5. Grau de explicabilidade exigido no relatório

---

## Riscos e mitigação
- **Risco:** dados em formatos inconsistentes
  - **Mitigação:** normalizador de entrada + checklist de upload
- **Risco:** baixa confiança no diagnóstico automático
  - **Mitigação:** exibir evidências e score de confiança por item
- **Risco:** escopo grande demais para primeira release
  - **Mitigação:** limitar v1 a 1 curso + 1 ciclo + 1 modelo de planilha

---

## Próximo passo recomendado
Rodar um workshop de 60–90 minutos para responder as perguntas da Fase 1 e congelar o escopo da v1 com critérios de aceite objetivos.
