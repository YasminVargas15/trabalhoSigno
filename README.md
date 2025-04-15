# trabalhoSigno

        //entrada de dados 
        int sexo, dia, mes, ano, idade, numeroSorte, numCor;
        String nome, signo, corSorte;
        Scanner ler = new Scanner(System.in);

        //solicitando as informações 
        System.out.println("Digite seu nome completo: ");
        nome = ler.nextLine();
        System.out.println("digite seu sexo (1 para Feminino, 2 para Masculino): ");
        sexo = ler.nextInt();
        System.out.println("Digite o dia de nascimento: ");
        dia = ler.nextInt();
        System.out.println("Digite o mês de nascimento: ");
        mes = ler.nextInt();
        System.out.println("Digite o ano de nascimento: ");
        ano = ler.nextInt();

        //caso a informação indicada pela pessoa esteja incorreta
        if (nome.length() < 8) {
            System.out.println("Seu nome não foi informado corretamente, deve contem mais do que 8 caracteres");
            return;
        }

        //gerando o numero da sorte e a cor da sorte 
        numeroSorte = 1 + (int) (Math.random() * 99);

        // validar data
        //validando idade
        Calendar hoje = Calendar.getInstance();
        int diaAtual = hoje.get(Calendar.DATE);
        int mesAtual = hoje.get(Calendar.MONTH) + 1;
        int anoAtual = hoje.get(Calendar.YEAR);

        //descobrindo a idade
        idade = anoAtual - ano;
        if (mes > mesAtual || (mes == mesAtual && dia > diaAtual)) {
            idade--;
        }

        //identificador do signo
        signo = "Aries";

        //dia e mes
        if (dia >= 1 && dia <= 31 && mes >= 1 && mes <= 12) {

            //descobrindo o Signo
            if ((mes == 3 && dia >= 21) || (mes == 4 && dia <= 20)) {
                signo = "Áries";

            } else if ((mes == 4 && dia >= 21) || (mes == 5 && dia <= 20)) {
                signo = "Touro";

            } else if ((mes == 5 && dia >= 21) || (mes == 6 && dia <= 20)) {
                signo = "Gêmeos";

            } else if ((mes == 6 && dia >= 21) || (mes == 7 && dia <= 21)) {
                signo = "Câncer";

            } else if ((mes == 7 && dia >= 22) || (mes == 8 && dia <= 22)) {
                signo = "leão";

            } else if ((mes == 8 && dia >= 23) || (mes == 9 && dia <= 22)) {
                signo = "virgem";

            } else if ((mes == 9 && dia >= 23) || (mes == 10 && dia <= 22)) {
                signo = "Libra";

            } else if ((mes == 10 && dia >= 23) || (mes == 11 && dia <= 21)) {
                signo = "Escorpião";

            } else if ((mes == 11 && dia >= 22) || (mes == 12 && dia <= 21)) {
                signo = "sagitario";

            } else if ((mes == 12 && dia >= 22) || (mes == 1 && dia <= 20)) {
                signo = "Capricórnio";

            } else if ((mes == 1 && dia >= 21) || (mes == 2 && dia <= 19)) {
                signo = "Aquário";

            } else if ((mes == 2 && dia >= 20) || (mes == 3 && dia <= 20)) {
                signo = "Peixes";
            }
        }

        //cor da sorte
        corSorte = "azul";

        numCor = 1 + (int) (Math.random() * 9);
        switch (numCor) {
            case 1:
                corSorte = "Vermelho";
                break;
            case 2:
                corSorte = "Verde";
                break;
            case 3:
                corSorte = "Preto";
                break;
            case 4:
                corSorte = "Branco";
                break;
            case 5:
                corSorte = "Laranja";
                break;
            case 6:
                corSorte = "Rosa";
                break;
            case 7:
                corSorte = "Roxo";
                break;
            case 8:
                corSorte = "Amarelo";
                break;
            default:
                corSorte = "Azul";
        }
        //saida de dados
        if (sexo == 1) {
            System.out.println("Sra. " + nome + ", nascida em " + dia + "/" + mes + "/" + ano + ", é do signo de " + signo + ". Você tem "
                    + idade + " anos. Seu número da sorte é " + numeroSorte + " e sua cor da sorte é " + corSorte);
        } else {
            System.out.println("Sr. " + nome + ", nascida em " + dia + "/" + mes + "/" + ano + ", é do signo de " + signo + ". Você tem "
                    + idade + " anos. Seu número da sorte é " + numeroSorte + " e sua cor da sorte é " + corSorte);
        }
    }
    }
