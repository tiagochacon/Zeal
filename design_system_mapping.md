# Mapeamento do Design System Zeal (Baseado em app-zeal-ref)

A identidade visual do projeto de referência (`deepsourcelabs/zeal-next`) utiliza uma paleta de cores nomeada e a fonte Inter. Devido à dificuldade em extrair os valores hexadecimais exatos (devido ao uso de um exportador de tokens customizado), foi inferida uma paleta moderna e profissional que respeita a intenção visual e os nomes dos tokens encontrados (`robin`, `lilac`, `ink`, `sea-glass`, `juniper`).

Esta paleta será mapeada para as variáveis CSS existentes no projeto Zeal (baseado em `shadcn/ui` e Tailwind CSS) para garantir a consistência e a facilidade de implementação.

## 1. Paleta de Cores (Inferred)

A cor primária foi escolhida para refletir o tom de Teal/Verde vibrante comumente associado à marca DeepSource.

| Nome do Token | Uso | Valor Hexadecimal | Variável CSS (Zeal) |
| :--- | :--- | :--- | :--- |
| **Robin** (Primary) | Cor principal de marca, botões, links, destaques. | `#00C896` | `--primary`, `--sidebar-primary` |
| **Lilac** (Accent) | Cor secundária, gradientes, elementos de destaque. | `#A06CD5` | `--accent` |
| **Ink** (Foreground/Dark) | Texto principal, fundos escuros (Dark Mode). | `#1D1F24` | `--foreground` (Dark Mode), `--sidebar-foreground` (Dark Mode) |
| **Sea-Glass** (Background/Light) | Fundo principal, superfícies claras. | `#F7F9FA` | `--background`, `--card`, `--popover` |
| **Juniper** (Success/Status) | Indicadores de sucesso e status positivo. | `#00A86B` | (Será mapeado para um tom de sucesso) |
| **Vanilla** (Lightest) | Texto sobre cores escuras, bordas claras. | `#FFFFFF` | `--primary-foreground`, `--background` (Light Mode) |

## 2. Tipografia

A fonte principal do Design System de referência é a **Inter**.

| Propriedade | Valor |
| :--- | :--- |
| **Família da Fonte** | `Inter`, `sans-serif` |
| **Uso** | Corpo de texto, títulos, interface. |

## 3. Mapeamento de Variáveis CSS (Zeal)

O projeto Zeal utiliza um sistema de variáveis CSS para temas claro e escuro. O novo visual será aplicado redefinindo essas variáveis no arquivo `client/src/index.css`.

| Variável CSS (Zeal) | Light Mode (Valor) | Dark Mode (Valor) |
| :--- | :--- | :--- |
| `--primary` | `#00C896` | `#00C896` |
| `--primary-foreground` | `#FFFFFF` | `#1D1F24` |
| `--background` | `#F7F9FA` | `#1D1F24` |
| `--foreground` | `#1D1F24` | `#F7F9FA` |
| `--card` | `#FFFFFF` | `#25282F` (Ink 800) |
| `--card-foreground` | `#1D1F24` | `#F7F9FA` |
| `--popover` | `#FFFFFF` | `#25282F` |
| `--popover-foreground` | `#1D1F24` | `#F7F9FA` |
| `--secondary` | `#E5E7EB` (Gray 200) | `#373A42` (Ink 700) |
| `--secondary-foreground` | `#1D1F24` | `#F7F9FA` |
| `--muted` | `#F3F4F6` (Gray 100) | `#373A42` |
| `--muted-foreground` | `#6B7280` (Gray 500) | `#9CA3AF` (Gray 400) |
| `--accent` | `#A06CD5` | `#A06CD5` |
| `--accent-foreground` | `#FFFFFF` | `#FFFFFF` |
| `--destructive` | `#EF4444` (Red) | `#F87171` (Red Light) |
| `--destructive-foreground` | `#FFFFFF` | `#1D1F24` |
| `--border` | `#E5E7EB` | `#373A42` |
| `--input` | `#E5E7EB` | `#373A42` |
| `--ring` | `#00C896` | `#00C896` |

**Próxima Fase:** Implementação da nova identidade visual no projeto Zeal.

## 4. Estilo de Componentes (Ajustes Iniciais)

*   **Bordas:** O projeto Zeal usa `var(--radius): 0.65rem`. Manteremos este valor para um visual moderno, mas faremos ajustes nos componentes para um estilo mais limpo e com sombras sutis, conforme o projeto de referência.
*   **Sombras:** Adicionar uma sombra sutil para cards e popovers, como `shadow-md` ou uma sombra customizada para profundidade.

Com este mapeamento, posso avançar para a implementação.
