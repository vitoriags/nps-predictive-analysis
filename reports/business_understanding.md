# 1. Entendimento do negócio

## Qual problema de negócio está sendo resolvido?

O problema de negócio está ligado à dificuldade da empresa em entender, de forma antecipada, o que faz um cliente terminar a jornada de compra satisfeito ou insatisfeito. Como se trata de um e-commerce com muitos pedidos, entregas e contatos com atendimento, algumas falhas na operação podem afetar bastante a experiência do cliente.

Hoje, o NPS só é coletado depois que a compra já foi finalizada. Ou seja, a empresa só descobre que houve uma experiência ruim quando o cliente já passou pelo problema e já avaliou a marca negativamente, dificultando uma atuação mais preventiva por parte das áreas envolvidas.

Por isso, o objetivo do projeto não é apenas olhar para a nota final do NPS, e sim, entender quais fatores da operação mais influenciam essa nota. A partir dessa análise, a empresa pode identificar padrões, priorizar melhorias e agir antes que mais clientes tenham experiências negativas ou se tornem detratores da marca.

## Por que o NPS é importante para um e-commerce?

O NPS é importante para um e-commerce porque ele ajuda a medir como o cliente percebeu a experiência de compra como um todo, não apenas uma etapa isolada. Em uma loja online, a satisfação do cliente pode ser influenciada por vários fatores, como prazo de entrega, atraso, valor do frete, facilidade de pagamento, necessidade de contato com o atendimento e resolução de problemas.

Por isso, o NPS funciona como um indicador que resume a percepção final do cliente depois da jornada de compra. Quando a nota é alta, pode existir uma chance maior de o cliente voltar a comprar e indicar a empresa para outras pessoas. Quando a nota é baixa, pode indicar problemas que afetam diretamente a fidelização, a reputação da marca e até a competitividade da empresa no mercado.

Neste projeto, o NPS é importante porque permite conectar dados operacionais com a experiência do cliente. Assim, a empresa consegue deixar de olhar apenas para indicadores internos, como tempo de entrega ou número de reclamações, e passa a entender como esses fatores realmente impactam a satisfação. Isso torna a análise mais útil para o negócio, porque ajuda a priorizar melhorias que podem gerar impacto real na experiência do consumidor.

## Quais áreas poderiam se beneficiar desses insights?

Esses insights poderiam ajudar várias áreas do e-commerce, porque a experiência do cliente não depende de uma única etapa. Ela começa no pedido, passa pelo pagamento, entrega, atendimento e só termina quando o cliente sente que a compra foi bem resolvida.

A área de logística seria uma das mais impactadas, já que atraso na entrega, tempo total de entrega, valor do frete e tentativas de entrega podem influenciar diretamente a satisfação do cliente. Se os dados mostrarem que esses fatores estão ligados a notas mais baixas de NPS, a empresa consegue priorizar melhorias na operação.

O atendimento ao cliente também se beneficiaria bastante, principalmente para entender se muitos contatos, reclamações ou demora na resolução dos problemas estão deixando os clientes mais insatisfeitos. Com isso, a empresa poderia agir mais rápido em casos críticos e evitar que o cliente termine a experiência com uma percepção negativa.

Além disso, áreas como produto, pricing e estratégia também poderiam usar esses resultados. Produto poderia observar se certos tipos de pedido geram mais insatisfação. Pricing poderia avaliar se frete, desconto ou valor do pedido afetam a percepção de custo-benefício. Já a área estratégica poderia usar a análise para decidir onde investir primeiro para melhorar a experiência, reduzir detratores e aumentar a chance de recompra.

## Como o NPS impacta recompra, boca a boca e market share?

O NPS pode impactar a recompra porque clientes satisfeitos podem confiar mais na empresa e voltar a comprar. Em um e-commerce, isso pesa bastante, já que o cliente normalmente tem muitas opções parecidas. Se a experiência for boa, com uma entrega dentro do esperado, bom atendimento e poucos problemas durante a compra, a chance de ele escolher a mesma loja novamente aumenta.

O boca a boca também é muito influenciado pela experiência do cliente. Quando o cliente fica satisfeito, ele pode recomendar a empresa para outras pessoas ou deixar avaliações positivas. Mas, se a experiência for ruim, ele pode reclamar, avaliar mal a loja e influenciar outras pessoas a não comprarem. No ambiente digital, isso pode ter um impacto ainda maior, porque uma reclamação pode ser vista por várias outras pessoas.

O market share pode ser afetado no longo prazo. Uma empresa que consegue manter mais clientes satisfeitos consegue fortalecer sua reputação, aumentar a fidelização e competir melhor com outros e-commerces. Já uma empresa com muitos clientes insatisfeitos pode acabar perdendo espaço para concorrentes que entregam uma experiência mais confiável.

Por isso, o NPS não deve ser visto apenas como uma nota de satisfação. Ele ajuda a empresa a entender se a experiência oferecida está ajudando a manter clientes, gerar recomendações e sustentar o crescimento no mercado.

## Quais indicadores de mercado poderiam complementar essa análise?

Além dos dados internos da empresa, alguns indicadores de mercado poderiam ajudar a complementar a análise. Um deles seria o benchmark de NPS do setor, para entender se a nota da empresa está boa ou ruim quando comparada com outros e-commerces. Olhar apenas para o NPS interno pode limitar a interpretação, porque uma nota pode parecer baixa, mas talvez esteja próxima da média do mercado, ou o contrário.

Um outro indicador importante seria o SLA logístico, como prazo médio de entrega, percentual de entregas no prazo e tempo médio de atraso em comparação com o mercado. Como a entrega é uma parte muito importante da experiência em e-commerce, esse tipo de comparação pode ajudar a entender se a empresa está abaixo, dentro ou acima do esperado pelos clientes.

Também seria útil acompanhar indicadores relacionados à concorrência, como avaliações em sites públicos, reclamações, reputação da marca, preço médio de frete, prazo de entrega prometido e políticas de troca ou devolução. Esses fatores podem influenciar a percepção do cliente, porque ele normalmente compara a experiência com outras lojas parecidas.

Assim, esses indicadores externos poderiam ajudar a empresa a interpretar melhor o NPS. Em vez de olhar apenas para a própria operação, ela conseguiria entender se os problemas encontrados são internos ou se também podem estar ligados ao nível de exigência e competição do mercado.

# 2. Definição da Target

## Qual variável representa a satisfação do cliente?

A variável que representa a satisfação do cliente neste projeto é a 'nps_score'. Ela mostra a nota dada pelo cliente depois da experiência de compra, em uma escala de 0 a 10.

## Por que ela foi escolhida?

Essa variável foi escolhida porque o NPS representa a percepção final do cliente sobre a jornada de compra.

## Em que momento da jornada essa informação é coletada?

Essa informação é coletada depois que a jornada de compra já foi encerrada. Ou seja, o cliente dá a nota depois de passar pelas etapas de pedido, pagamento, entrega e possíveis contatos com atendimento.

## Existe algum risco de usar essa variável de forma inadequada?

Sim. Um risco é tratar o NPS como se ele explicasse sozinho toda a experiência do cliente. A nota pode ser influenciada por vários fatores ao mesmo tempo, como atraso, atendimento, valor do frete e etc...

Outro cuidado é não confundir relação com causa. Por exemplo, se clientes com atraso na entrega têm NPS menor, isso pode indicar uma relação importante, mas ainda precisa ser analisado com cuidado antes de afirmar que o atraso foi a única causa da insatisfação dele.