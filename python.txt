precoUnitario = float(input("Digite o preço unitário"))
totalImposto = 0

while precoUnitario > 0:

 if precoUnitario > 0:
     
  pais = int(input("\n\nDigite o país:\n\n[1] EUA\n\n[2] MÉXICO\n\n[3]Outro\n\n"))
  
  if pais == 0:
      print ("\n\nPrograma finalizado.")

      from sys import exit
      exit()
  
  else:
   
   while pais != 1 and pais != 2 and pais != 3:
       print ("País inválido. Digite novamente.")
   
       pais = int(input("\n\nDigite o país:\n\n[1] EUA\n\n[2] MÉXICO\n\n[3]Outro\n\n"))
       
   transporte = (input("\n\nQual o tipo de transporte? Digite em CAIXA ALTA.\n\n[T] TERRESTRE\n\n[A] AÉREO\n\n[F] FLUVIAL\n\n"))
  
  if transporte == ('0'):
      
   print ("\n\nPrograma finalizado.")
   
   from sys import exit
   exit()
      
  else:
   
  
   while transporte != 'A' and transporte != 'T' and transporte != 'F':
    
      print ("Tipo de transporte inválido. Digite novamente")
    
      transporte = (input("\n\nQual o tipo de transporte? Digite em CAIXA ALTA.\n\n[T] TERRESTRE\n\n[A] AÉREO\n\n[F] FLUVIAL\n\n"))
    
  tipoCarga = (input("\n\nPossui carga perigosa? Digite em CAIXA ALTA.\n\n[S] Sim[N] Não\n\n"))
      
  if tipoCarga == ('0'):
      
     print ("\n\nPrograma finalizado.")
   
     from sys import exit
     exit()
      
  else:
   
   while tipoCarga != ('S') and tipoCarga != ('N'):
       
    print ("\n\nTipo de carga inválido. Digite novamente.")
    tipoCarga = (input("\n\nPossui carga perigosa? Digite em CAIXA ALTA.\n\n[S] Sim[N] Não\n\n"))
    
   if tipoCarga == ('S'):
      if pais == 1:
        vt = 50
      else: 
       if pais == 2:
        vt = 21
       else:
        vt = 24
        
   else:
       if tipoCarga == ('N'):
        if pais == 1:
         vt = 12
        else:
         if pais == 2:
          vt = 21
         else:
           vt = 60
        
          
       
  
  
 if precoUnitario <= 100:
      imposto = 0.05*precoUnitario
 else:
      imposto = 0.1*precoUnitario
      
  
 if pais == 2 or transporte == ('A'):
     seguro = precoUnitario/2
 else:
     seguro = 0


 print ("\n\nPreço final =",precoUnitario + imposto + vt + seguro)
   
 totalImposto = totalImposto + imposto


 print("Total de impostos =", totalImposto)
  
 precoUnitario = float(input("Digite o preço unitário"))
 
print ("Programa finalizado.")

 

 