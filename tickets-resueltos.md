# 🎫 Registro de Tickets - Help Desk IT
**Autor:** Sofia Dearriba | Soporte Técnico N1

---

## TKT-001 | Impresora sin respuesta

| Campo | Detalle |
|-------|---------|
| **Fecha apertura** | 2025-03-10 09:15 |
| **Usuario** | María González - Administración |
| **Prioridad** | Media |
| **Categoría** | Hardware / Periféricos |

**Descripción del problema:**  
La usuaria reporta que al intentar imprimir un documento desde Word, la impresora HP LaserJet no responde. El trabajo queda en cola pero no se imprime.

**Diagnóstico:**  
- Impresora encendida y conectada físicamente ✅
- Cola de impresión con 3 trabajos atascados ⚠️
- Servicio Print Spooler en estado "detenido" ❌

**Solución aplicada:**  
1. Detención del servicio Spooler via CMD
2. Eliminación de archivos en C:\Windows\System32\spool\PRINTERS
3. Reinicio del servicio Spooler
4. Prueba de impresión exitosa

**Tiempo de resolución:** 8 minutos  
**Estado:** ✅ CERRADO - Resuelto en N1

---

## TKT-002 | Sin acceso a Internet

| Campo | Detalle |
|-------|---------|
| **Fecha apertura** | 2025-03-12 14:30 |
| **Usuario** | Carlos Pérez - Ventas |
| **Prioridad** | Alta |
| **Categoría** | Redes / Conectividad |

**Descripción del problema:**  
El usuario no puede acceder a ninguna página web ni al correo corporativo. WiFi muestra conectado pero sin acceso a Internet.

**Diagnóstico:**  
```
ipconfig → IP: 169.254.45.12 (APIPA - sin DHCP)
ping 192.168.1.1 → Request timeout
ping 8.8.8.8 → Request timeout
```
El equipo no está obteniendo IP del servidor DHCP.

**Solución aplicada:**  
1. Ejecución de ipconfig /release y /renew
2. Sin resultado → reseteo de adaptador de red
3. Reinicio del equipo
4. IP asignada correctamente: 192.168.1.45
5. Navegación restaurada

**Tiempo de resolución:** 12 minutos  
**Estado:** ✅ CERRADO - Resuelto en N1

---

## TKT-003 | Olvido de contraseña

| Campo | Detalle |
|-------|---------|
| **Fecha apertura** | 2025-03-15 08:05 |
| **Usuario** | Laura Romero - RRHH |
| **Prioridad** | Baja |
| **Categoría** | Gestión de cuentas / Accesos |

**Descripción del problema:**  
La usuaria olvidó su contraseña de Windows y no puede ingresar al equipo.

**Diagnóstico:**  
- Cuenta de dominio activa ✅
- Sin bloqueo por intentos fallidos ✅
- Requiere reset de contraseña por administrador

**Solución aplicada:**  
1. Verificación de identidad de la usuaria (DNI + legajo)
2. Reset de contraseña desde consola de administración (Active Directory)
3. Contraseña temporal asignada con obligación de cambio al primer login
4. Comunicación de nueva contraseña por canal seguro

**Tiempo de resolución:** 5 minutos  
**Estado:** ✅ CERRADO - Resuelto en N1

---

## TKT-004 | PC lenta / alto uso de CPU

| Campo | Detalle |
|-------|---------|
| **Fecha apertura** | 2025-03-18 11:20 |
| **Usuario** | Roberto Silva - Contabilidad |
| **Prioridad** | Media |
| **Categoría** | Rendimiento del sistema |

**Descripción del problema:**  
El usuario reporta que su PC está muy lenta desde hace dos días. Los programas tardan en abrir y el ventilador hace ruido constante.

**Diagnóstico:**  
- Uso de CPU: 95% constante (Administrador de Tareas)
- Proceso consumidor: antivirus en escaneo programado + Windows Update en segundo plano
- Espacio en disco C: 98% ocupado ⚠️

**Solución aplicada:**  
1. Pausa temporal del escaneo de antivirus
2. Limpieza de archivos temporales (liberados 4.2 GB)
3. Vaciado de Papelera de Reciclaje
4. Desinstalación de programas no utilizados
5. Reprogramación de tareas automáticas fuera del horario laboral
6. CPU normalizado al 15-20%

**Tiempo de resolución:** 20 minutos  
**Estado:** ✅ CERRADO - Resuelto en N1

---

*Registro generado con fines de práctica en gestión de incidencias IT - ITIL N1*  
*Autor: Sofia Dearriba | github.com/sofia-dearriba*
