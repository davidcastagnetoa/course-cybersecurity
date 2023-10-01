## Organización de Máquinas en el AD

Por defecto, todas las máquinas que se unen a un dominio se colocan en el contenedor "Computers", aquí se hallan diversos dispositivos como servidores, laptops y PCs.

![Managing Computers in Active Directory](/images/Managing-Computers-AD-01.png)

### Organización Ideal:

- **Estaciones de Trabajo (Workstations):**
  Cada usuario en el dominio probablemente inicie sesión en una de estas, usándola para sus actividades diarias de trabajo o navegación.
- **Servidores:**
  Usados generalmente para proporcionar servicios a usuarios u otros servidores.
- **Controladores de Dominio:**
  Permiten administrar el Dominio de Active Directory y son considerados los dispositivos más sensibles dentro de la red.

  ![Managing Computers in Active Directory](/images/Managing-Computers-AD-02.png)

### Creación de Unidades Organizativas (OUs):

Para una mejor organización, crearemos dos OUs separadas, una para Estaciones de Trabajo y otra para Servidores, y moveremos las máquinas correspondientes a sus respectivas OUs. Así, podremos configurar políticas específicas para cada OU.

```plaintext
thm.local
│
├── Workstations
│   ├── PC1
│   ├── Laptop1
├── Servers
│   ├── Server1
└── Domain Controllers
    └── DC1
```
