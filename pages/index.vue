<template>
    <div class="index">
        <v-container class="index-first">
            <div class="banner mt-4 mb-16 mx-auto">
                <v-img src="/banner.jpg" max-width="100%" contain />
            </div>
            <ActionListList :items="actionList" />
            <h1 class="program-header mt-16 mb-2">Programa</h1>
            <Program :items="programItems" />
        </v-container>
        <div
            id="candidatos"
            class="candidatos iniciativa-blue white--text my-16"
        >
            <v-container>
                <h1 class="my-4">Os nossos candidatos</h1>
                <Candidates :candidates="candidates" />
            </v-container>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        actionList: {
            type: Array,
            default: () => [
                {
                    first: "Mais",
                    second: "Transparência",
                    lines: [
                        "Atas e gravações para todos",
                        "Levantamento e publicação de todo o património do município",
                        "Criação de um provedor do munícipe"
                    ]
                },
                {
                    first: "Trabalhar",
                    second: "Em Gaia",
                    lines: [
                        "Redução da taxa de derrama para o valor mínimo",
                        "Criação de um portal para captar o investimento a nível local",
                        "Simplificação de processos administrativos, legalização e fiscalização"
                    ]
                },
                {
                    first: "Liberdade",
                    second: "De movimentos",
                    lines: [
                        "Criação de uma rede de transportes municipais",
                        "Garantir a execução atempada e rigorosa do ponto de vista financeiro, da 2ª linha de Gaia"
                    ]
                }
            ]
        },
        programItems: {
            type: Array,
            default: () => [
                {
                    header: "Transparência",
                    content: [
                        "Disponibilização das atas e gravações do executivo camarário e Assembleia Municipal no sítio da internet do município",
                        "Declaração de registo de interesses e declaração patrimonial de todos os membros da câmara e deputados municipais",
                        "Levantamento e Publicação de todo o património do Município",
                        "Criação de uma área de transparência",
                        "Criação de um provedor do munícipe"
                    ]
                },
                {
                    header: "Atratividade e competitividade empresarial",
                    content: [
                        "Redução da taxa de derrama para o valor mínimo",
                        "Criação de um portal para captar o investimento a nível local",
                        "Criação de um portal para navegação do património do município para captação de investimento e fixação de empresas",
                        "Reforçar a aposta no Licenciamento Zero",
                        "Simplificação de processos administrativos, legalização e fiscalização",
                        "Diminuição da participação da Câmara Municipal em entidades municipais, privilegiando a concessão",
                        "Dinamização da estrutura INOVAGAIA como gabinete de prospeção e captação de empresas e investimento",
                        "Reestruturação do regulamento municipal de atribuição de benefícios com o foco de promover a criação de emprego e diversificação económica"
                    ]
                },
                {
                    header: "Mobilidade",
                    content: [
                        "Ser um parceiro ativo da requalificação da ligação Nascente/Poente ao Porto",
                        "Criação de uma rede de transportes municipais, num modelo de hub intermodal de mobilidade combinada",
                        "Garantir a execução atempada e rigorosa do ponto de vista financeiro, da 2ª linha de Gaia",
                        "Recuperação da discussão da ponte pedonal Gaia-Porto como um ponto de captação turística do Porto e desenvolvimento económico da margem de Gaia",
                        "Implementação do sistema kiss & ride, em todas as escolas e estações de comboio do município",
                        "Criação de uma malha de ciclovias com epicentro nos hubs intermodais"
                    ]
                },
                {
                    header: "Reforma fiscal e despesa pública",
                    content: [
                        "Devolução da participação de IRS (4%) para financiamento municipa",
                        "Implementação de orçamento de base zero",
                        "Redução de IMI para a taxa mínima legalmente prevista e dedução fixa para famílias numerosas",
                        "Mapeamento das propriedades do município identificando as mais-valias e as elegíveis para alienação",
                        "Princípio da autossuficiência para todas as associações e instituições"
                    ]
                },
                {
                    header: "Educação",
                    content: [
                        "Sistema de cheque-ensino promovendo a liberdade de escolha das famílias relativamente à escola pública ou privada",
                        "Reforço das bolsas de mérito",
                        "Aproximação das instituições de ensino ao tecido empresarial do concelho",
                        "Criação de programas de ensino de literacia económica e financeira",
                        "Aumentar envolvimento da sociedade escolar com os organismos municipai",
                        "Promover maior autonomia na intervenção das escolas TEIP, de forma promover a reabilitação e sucesso da comunidade estudantil",
                        "Promover a criação de um Hub Universitário/Politécnico, aproximando a comunidade do ensino superior fixando-o na cidade",
                        "Fomentar as ligações às Universidades e respetivas associações e federações como agentes ativos do desenvolvimento económico e social"
                    ]
                },
                {
                    header: "A CONTINUAR ..."
                }
            ]
        },
        candidates: {
            type: Array,
            default: () => [
                {
                    title: "Orlando Monteiro da Silva",
                    subtitle: "Câmara Municipal de Gaia",
                    photo: "https://picsum.photos/600"
                },
                {
                    title: "Rui Leite de Castro",
                    subtitle: "Assembleia Municipal de Gaia",
                    photo: "https://picsum.photos/600"
                },
                {
                    title: "Miguel Monteiro dos Santos",
                    subtitle: "Junta de Freguesia de Vilar de Andorinho",
                    photo: "https://picsum.photos/600"
                },
                {
                    title: "Pedro Matos",
                    subtitle:
                        "Junta de Freguesia de Mafamude e Vilar do Paraíso",
                    photo: "https://picsum.photos/600"
                }
            ]
        }
    }
}
</script>

<style>
.index > .index-first > .banner {
    max-width: 800px;
}

.index > .index-first > .program-header {
    color: #000085;
    text-transform: uppercase;
}
</style>
