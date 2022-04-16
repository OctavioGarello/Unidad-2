class Email:
    __idCuenta= ""
    __dominio= ""
    __tipodominio= ""
    __contrasena= ""
    def __init__(self,idcuenta,dominio,tipodominio,contrasena=None): #crear objeto
        self.__idCuenta=idcuenta #self es referencia
        self.__dominio=dominio
        self.__tipodominio=tipodominio
        self.__contrasena=contrasena
    def retornaEmail(self):
        return(self.__idCuenta+"@"+self.__dominio+"."+self.__tipodominio)

    def getIdcuenta(self):
        return(self.__idCuenta)

    def getDominio(self):
        return(self.__dominio)

    def cambiarContra(self,actual,nueva):
        if(actual==self.__contrasena):
            self.__contrasena=nueva
            print("Guardado Exitosamente")
        else:
            print("ERROR: La contraseña no coincide")

    @staticmethod
    def crearCuenta(correo):
        x=correo.split("@")
        newid=x[0]
        y=x[1].split(".")
        newdom=y[0]
        newtip=y[1]
        return Email(newid,newdom,newtip)


if __name__ == "__main__":
    print("------------")
    nom=input("Ingrese su Nombre: ")
    nomu=input("Nombre Usuario: ")
    id=input("IdCuenta: ")
    dom=input("Dominio: ")
    tdom=input("Tipo de Dominio: ")
    cont=input("Contraseña: ")
    email1 = Email(id, dom, tdom, cont)

    print("------------")
    print("Estimado "+nom+" te enviaremos tus mensajes a la dirección "+email1.retornaEmail()+".")
    print("------------")
    print("#Modificar Contraseña")
    actual=input("Ingrese Contraseña Actual: ")
    nueva=input("Ingrese Nueva Contraseña: ")
    email1.cambiarContra(actual,nueva)

    print("------------")
    nueco=input("#Ingrese Correo:")
    nuevo=Email.crearCuenta(nueco)
    print(nuevo.retornaEmail())

    print("------------")
    print("#Leer Archivo")
    identificador=input("Ingresa Id: ")

    archivo=open('archivo.txt','r')
    x=archivo.readline()
    lista=x.split(",")
    i=0
    for xcorreo in lista:
        instancia=Email.crearCuenta(xcorreo)
        #print(instancia.getIdcuenta())
        if(instancia.getIdcuenta()==identificador):
            i=1

    if(i==1):
        print("Se repite Identificador")
    else:
        print("No se repite")
