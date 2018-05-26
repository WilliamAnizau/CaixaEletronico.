public CaixaEletronico() {

saldo = "0";
codigo = "BAB321";
numero = "1";
endereco = "Rua Montese";
cidade = "Sumare";
estado = "Sao Paulo";

Bandeja(){
    
}

 Bandeja bandeja1 = new Bandeja(){
 bandeja1.ValorDaFace=10;
 bandeja1.QuantidadeDeCeddula=10;
 };

 Bandeja bandeja2 = new Bandeja();
 bandeja2.ValorDaFace=20;
 bandeja2.QuantidaDeDeCedula=50;

 Bandeja bandeja3 = new Bandeja();
 bandeja3.ValorDaFace=100;
 bandeja3.QuantidadeDeCedula=20; 

 private Bandeja bandeja4 = new Bandeja();
 bandeja4.ValorDaFace=50;
 bandeja4.QuantidadeDeCedula=30;
 }
public static void main(String[]args) {

Bandeja bandeja1 = new Bandeja(); Bandeja bandeja2 = new Bandeja(); Bandeja bandeja3 = new Bandeja(); Bandeja bandeja4 = new Bandeja(); CaixaEletronico(); saldo = Saldo(); saldoDaBandeja = SaldoDaBandeja(bandeja1); Sacar(50,bandeja2);

}

   public int Saldo(){

 int totalBandeja1 = bandeja1.ValorDaFace * bandeja1.QuantidadeDeCedula;

 int totalBandeja2 = bandeja2.ValorDaFace * bandeja2.QuantidadeDeCedula;

 int totalBandeja3 = bandeja3.ValorDaFace * bandeja3.QuantidadeDeCedula;

 int totalBandeja4 = bandeja4.ValorDaFace * bandeja4.QuantidadeDeCedula;

   saldo = totalBandeja1+totalBandeja2+totalBandeja3+totalBandeja4; 

 return saldo; 
} public int SaldoDaBandeja(Bandeja bandeja){

int totalBandeja = bandeja.ValorDaFace * bandeja1.QUantidadeDeCedula;
return totalBandeja;
}

public void Sacar(int valor,Bandeja bandeja){

int total = bandeja.ValorDaFace * bandeja.QuantidadeDeCedula; 

  if (total <= valor) { 

    total = total - valor;
    

    int[] cedulas = {100,50,25,10};

    for(int i = 0; i < cedulas.length; i++){
    if( valor >= cedulas[i] ){
		System.out.println( (int)valor/cedulas[i] + " notas de " + cedulas[i]);
			valor = valor % cedulas[i];

                          } 
   }
  }
   else {
      	System.out.println("ValorDoSaque e maior que o saldo");
 
}
 
} 
}
