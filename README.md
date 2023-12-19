#include <stdio.h>
#include <string.h>
#include <math.h>


int main() {
    int inicial, secundario,j; 
    char binario[100],opcao;
    int decimal=0,octal=0, hexadecimal=0;
    
    do{
    	system("cls");
	printf("=================================================BEM VINDO AO CONVERSOR=================================================\n\n");
    printf(" BASE INICAL:\n\n  1- para binario:\n  2- para decimal:\n  3- para hexadecimal:\n  4- para octal:\n  ");
    scanf("%d", &inicial);
    printf("\n BASE PARA CONVERSAO:\n\n  1- para binario:\n  2- para decimal:\n  3- para hexadecimal:\n  4- para octal:\n  ");
    scanf("%d", &secundario);

    if (inicial!=secundario && inicial >= 1 && inicial <= 4 && secundario >= 1 && secundario <= 4) {
        switch ((inicial - 1) * 4 + (secundario - 1)) {
            case 0:
                break;
            case 1:
                printf("\nConversao de binario para decimal\n");
                printf("Digite o numero binario: ");
                scanf("%s:\n", binario);
                int len = strlen(binario);
                decimal = 0;
                int i;
                for (i = len - 1; i >=0; i--) {
                    if (binario[i] == '1') {
                        decimal += pow(2, len - i -1);
                    }
                }
                printf("O numero binario %s em decimal seria: %d\n", binario, decimal);
                			
				fflush(stdin);
                break;                
            case 2:
                fflush(stdin);
                printf("\nConversao de binario para hexadecimal\n");
                printf("Digite o numero binario: ");
                scanf("%s:\n", binario);
                len = strlen(binario);
                decimal = 0;
                for (i = len - 1; i >=0; i--) {
                    if (binario[i] == '1') {
                        decimal += pow(2, len - i -1);
                    }
                }
                printf("O numero binario %s em hexadecimal seria: %x\n", binario, decimal);
                				
				fflush(stdin);
                break;
	        case 3:
	            printf("\nConversao de binario para octal\n");
                printf("Digite o numero binario: ");
                scanf("%s:\n", binario);
                len = strlen(binario);
                decimal = 0;
                for (i = len - 1; i >=0; i--) {
                    if (binario[i] == '1') {
                        decimal += pow(2, len - i -1);
                    }
                }
                printf("O numero binario %s em octal seria: %o\n", binario, decimal);              
				
				fflush(stdin);
                break;
			case 4:
			    printf("\nConversao de decimal para binario\n");
			    printf("Digite o numero decimal: ");
			    scanf("%d:\n", &decimal);
			    itoa(decimal, binario, 2);
			    printf("O numero octal %d em binario seria: %s\n", decimal, binario);		   
			   
			    fflush(stdin);
			    break;
	        case 6:
	            printf("\nConversao de decimal para hexadecimal\n");
	            printf("Digite o numero decimal: ");
				scanf("%d:\n", &decimal);
			    printf("O numero decimal %d em hexadecimal seria: %x\n", decimal, decimal);
			    fflush(stdin);
	
	            break;
	        case 7:
	            printf("\nConversao de decimal para octal\n");
	            printf("Digite o numero decimal: ");
	            scanf("%d:\n", &decimal);
			    printf("O numero decimal %d em octal seria: %o\n", decimal, decimal);
			    	
				fflush(stdin);	
	            break;
	        case 8:
	            printf("\nConversao de hexadecimal para binario\n");
	            printf("Digite o numero hexadecimal: ");
	            scanf("%x:\n", &hexadecimal);
			    itoa(hexadecimal, binario, 2);
			    printf("O numero octal %x em binario seria: %s\n", hexadecimal, binario);
	
				fflush(stdin);	
	            break;
	        case 9:
	        	decimal=0, hexadecimal=0;
	            printf("\nConversao de hexadecimal para decimal\n");
	            printf("Digite o numero hexadecimal: ");
	            scanf("%x:\n", &hexadecimal);
			    printf("O numero hexadecimal %x em decimal seria: %d\n", hexadecimal, hexadecimal);
			    fflush(stdin);	
		
	            break;
	        case 11:
	        	decimal=0, hexadecimal=0;
	            printf("\nConversao de hexadecimal para octal\n");
	            printf("Digite o numero hexadecimal: ");
	            scanf("%x:\n", &hexadecimal);
			    printf("O numero hexadecimal %x em octal seria: %o\n", hexadecimal, hexadecimal);		    
				
				fflush(stdin);	
	            break;
	        case 12:
	            printf("\nConversao de octal para binario\n");
	            printf("Digite o numero octal: ");
	            scanf("%o:\n", &octal);
			    itoa(octal, binario, 2);
			    printf("O numero octal %o em binario seria: %s\n", octal, binario);
		    				
				fflush(stdin);	
	            break;
	        case 13:
	        	octal=0, decimal=0;
	            printf("\nConversao de octal para decimal\n");
	            printf("Digite o numero octal: ");
	            scanf("%o:\n", &octal);
			    printf("O numero octal %o em decimal seria: %d\n", octal, octal);
			    				
				fflush(stdin);		
	            break;
	        case 14:
	        	octal=0, hexadecimal=0;
	            printf("\nConversao de octal para hexadecimal\n");
	            printf("Digite o numero octal: ");
	            scanf("%o:\n", &octal);
			    printf("O numero octal %o em hexadecimal seria: %x\n", octal, octal);
			    				
				fflush(stdin);		
	            break;       
	        }
	    }
	    printf("\nDeseja continuar? (s/n): ");
        scanf(" %c", &opcao);
	    }while  (opcao != 'n');	    
return 0;
	}
