# Farmacia Podología - Sistema de Gestión

Sistema completo de gestión de farmacia para clínica podológica con autenticación, inventario, ventas y compras a proveedores.

## Características

- ✅ Autenticación con JWT (email + contraseña)
- ✅ Roles de usuario (ADMIN y EMPLEADO)
- ✅ Gestión de productos e inventario
- ✅ CRUD de clientes
- ✅ CRUD de proveedores
- ✅ Módulo de compras a proveedores
- ✅ Módulo de ventas con carrito
- ✅ Historial de transacciones
- ✅ Dashboard con KPIs
- ✅ Gestión de usuarios (ADMIN)

## Stack Tecnológico

- **Frontend**: Next.js 15 + React 19 + TypeScript
- **Backend**: Next.js API Routes
- **Database**: PostgreSQL (Neon)
- **ORM**: Prisma 6
- **Autenticación**: JWT + Cookies HTTP-only
- **Contraseñas**: bcrypt
- **Estilos**: Tailwind CSS + shadcn/ui
- **Icons**: Lucide React

## Instalación

### 1. Clonar e instalar dependencias

\`\`\`bash
git clone <repo-url>
cd farmacia-podologia
npm install
\`\`\`

### 2. Configurar variables de entorno

Copiar `.env.example` a `.env.local`:

\`\`\`bash
cp .env.example .env.local
\`\`\`

Luego actualizar `DATABASE_URL` con tu conexión de Neon:

\`\`\`env
DATABASE_URL="postgresql://USER:PASSWORD@HOST:PORT/DBNAME?sslmode=require"
JWT_SECRET="tu_llave_secreta_aqui"
NEXT_PUBLIC_APP_URL="http://localhost:3000"
\`\`\`

### 3. Ejecutar migraciones de Prisma

\`\`\`bash
npx prisma generate
npx prisma migrate dev --name init
\`\`\`

Esto creará las tablas y ejecutará el seed automáticamente.

### 4. Iniciar el servidor de desarrollo

\`\`\`bash
npm run dev
\`\`\`

La aplicación estará disponible en: https://podocare-syste.vercel.app/login

## Credenciales de Demo

- **Email**: admin@farmacia.com
- **Contraseña**: password123
- **Rol**: ADMIN


## Scripts Disponibles

\`\`\`bash
# Desarrollo
npm run dev

# Build para producción
npm run build

# Iniciar servidor de producción
npm start

# Generar cliente de Prisma
npm run prisma:generate

# Ejecutar migraciones
npm run prisma:migrate

# Seed de base de datos
npm run prisma:seed

# Abrir Prisma Studio
npm run prisma:studio
\`\`\`

## Funcionalidades Clave

### Sistema de Inventario
- Stock automático actualizado en compras y ventas
- Alertas de stock bajo
- Histórico de movimientos

### Control de Acceso
- Autenticación basada en JWT
- Cookies HTTP-only seguras
- Middleware de protección de rutas
- Control de roles (ADMIN/EMPLEADO)

### Transacciones Comerciales
- Ventas con múltiples productos
- Carrito de compra
- Compras a proveedores
- Métodos de pago variables
- Información opcional de receta médica

### Reportes
- Dashboard con KPIs del día
- Historial completo de ventas
- Historial de compras
- Productos con stock bajo

## Despliegue en Vercel

1. Conectar repositorio en Vercel
2. Configurar variables de entorno
3. Configurar base de datos Neon en proyecto Vercel
4. Deploy automático en git push

## Desarrollo Futuro

- [ ] Descarga de reportes en PDF
- [ ] Integración con sistema de citas
- [ ] Dashboard avanzado con gráficos
- [ ] Sistema de notificaciones
- [ ] Backup automático
- [ ] API de socios externos
- [ ] App mobile

## Soporte

Para reportar bugs o solicitar features, contacta al equipo de desarrollo.
