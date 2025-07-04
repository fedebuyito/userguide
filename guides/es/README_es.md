# Guía de Usuario de SeedSigner

<div align="center">
  <img src="/guides/en/images/SeedSigner_Logo.png" alt="Logo de SeedSigner" width="400"/>
</div>

SeedSigner es un dispositivo de firma de Bitcoin de código abierto y aislado de cualquier conexión digital que te ayuda a gestionar tus semillas y firmar transacciones de forma segura. Esta guía proporciona instrucciones paso a paso organizadas por flujos de trabajo.

## 📋 Tabla de Contenidos

### 🚀 Primeros Pasos

- [Configuración Inicial y Encendido](/guides/es/getting_started/initial_setup_and_power_on.md)
- [Fundamentos de Navegación](/guides/es/getting_started/navigation_basics.md)
- [Apagado Seguro](/guides/es/getting_started/powering_off_safely.md)
- [Reiniciar tu Dispositivo](/guides/es/getting_started/restarting_your_device.md)
***REVISADO HAST AQUI***FEDEBUYITO
### 🌱 Gestión de Semillas

- **Crear Nuevas Semillas**
  - [Generación de Semilla Basada en Cámara](/guides/es/seed_management/creating_new_seeds/camera_based_seed_generation.md)
  - [Generación de Semilla Basada en Dados](/guides/es/seed_management/creating_new_seeds/dice_based_seed_generation.md)
  - [Generación de Semilla Calculando la 12ª/24ª Palabra](/guides/es/seed_management/creating_new_seeds/calc_12th24th_word_seed_generation.md)
- **Cargar Semillas Existentes**
  - [Entrada Manual de Semilla](/guides/es/seed_management/load_existing_seeds/manual_seed_entry.md)
  - [Escaneo de SeedQR](/guides/es/seed_management/load_existing_seeds/seedqr_scanning.md)
  - [Agregar Frase de Paso BIP-39](/guides/es/seed_management/load_existing_seeds/adding_bip_39_passphrase.md)

### 🔧 Trabajar con Semillas Cargadas

- [Exportar Clave Pública (Xpub)](/guides/es/working_with_loaded_seeds/export_public_key_xpub.md)
- [Generar Dirección de Recepción](/guides/es/working_with_loaded_seeds/generate_receiving_addresses.md)
- [Generar Cambio de Dirección](/guides/es/working_with_loaded_seeds/generate_change_addresses.md)
- [Ver Palabras Clave](/guides/es/working_with_loaded_seeds/view_seed_words.md)
- [Crear copia de seguridad de SeedQR](/guides/es/working_with_loaded_seeds/create_seedqr_backup.md)

### ✍️ Transacciones y Verificación

- [Firmar Transacción de Bitcoin (PSBT)](/guides/es/transactions_and_verification/sign_bitcoin_transaction_psbt.md)
- [Verificar Propiedad de Dirección](/guides/es/transactions_and_verification/verify_address_ownership.md)
- [Descartar Semilla Cargada](/guides/es/transactions_and_verification/discard_loaded_seed.md)

### ⚙️ Configuración del Dispositivo

- **Configuraciones Básicas**
  - [Configuración de Idioma](/guides/es/device_configuration/basic_settings/language_configuration.md)
  - [Configuraciones Persistentes](/guides/es/device_configuration/basic_settings/persistent_settings.md)
  - [Soporte de Software Coordinador](/guides/es/device_configuration/basic_settings/coordinator_software_support.md)
  - [Visualización de Denominación](/guides/es/device_configuration/basic_settings/denomination_display.md)
  - [Prueba de E/S de Hardware](/guides/es/device_configuration/basic_settings/hardware_io_testing.md)
  - [Información de Donaciones](/guides/es/device_configuration/basic_settings/donation_information.md)

- **Configuraciones Avanzadas**
  - [Selección de Red Bitcoin](/guides/es/device_configuration/advanced_settings/bitcoin_network_selection.md)
  - [Densidad de Código QR](/guides/es/device_configuration/advanced_settings/qr_code_density.md)
  - [Configuración de Exportación Xpub](/guides/es/device_configuration/advanced_settings/xpub_export_configuration.md)
  - [Configuración de Tipos de Firma](/guides/es/device_configuration/advanced_settings/signature_types_configuration.md)
  - [Configuración de Tipos de Script](/guides/es/device_configuration/advanced_settings/script_types_configuration.md)
  - [Mostrar Detalles de Xpub](/guides/es/device_configuration/advanced_settings/show_xpub_details.md)
  - [Configuración de Frase de Paso BIP-39](/guides/es/device_configuration/advanced_settings/bip-39_passphrase_configuration.md)
  - [Rotación de Cámara](/guides/es/device_configuration/advanced_settings/camera_rotation.md)
  - [SeedQR Compacto](/guides/es/device_configuration/advanced_settings/compact_seedqr.md)
  - [Semillas Hijas BIP-85](/guides/es/device_configuration/advanced_settings/bip-85_child_seeds.md)
  - [Semillas Electrum](/guides/es/device_configuration/advanced_settings/electrum_seeds.md)
  - [Firma de Mensajes](/guides/es/device_configuration/advanced_settings/message_signing.md)
  - [Advertencias de Privacidad](/guides/es/device_configuration/advanced_settings/privacy_warnings.md)
  - [Advertencias Graves](/guides/es/device_configuration/advanced_settings/dire_warnings.md)
  - [Consejos de Brillo QR](/guides/es/device_configuration/advanced_settings/qr_brightness_tips.md)
  - [Logos de Socios](/guides/es/device_configuration/advanced_settings/partner_logos.md)

- **Configuraciones de Hardware**
  - [Configuración de Tipo de Pantalla](/guides/es/device_configuration/hardware_settings/display_type_configuration.md)
  - [Inversión de Color](/guides/es/device_configuration/hardware_settings/color_inversion.md)

### 🔧 Soporte y Recursos

- [Solución de Problemas](/guides/es/support_and_resources/troubleshooting.md)
- [Recursos Adicionales](/guides/es/support_and_resources/additional_resources.md)
- [Consideraciones de Seguridad](/guides/es/support_and_resources/security_considerations.md)

> 💡 **Consejo de Navegación Rápida**: Usa Ctrl+F (o Cmd+F en Mac) para buscar temas específicos dentro de esta guía.

---

## Componentes de Hardware

Un dispositivo SeedSigner consta de:

1. **Raspberry Pi Zero** - La unidad de procesamiento principal
2. **Cámara Raspberry Pi** - Para escanear códigos QR y capturar entropía
3. **WaveShare 1.3inch LCD Hat** - Pantalla e interfaz de control

### Controles del LCD Hat WaveShare

<div align="center">
  <img src="/guides/en/images/WaveShare_LCD_Hat.png" alt="WaveShare LCD Hat" width="350"/>
</div>

El LCD Hat WaveShare proporciona los siguientes controles:

- **Joystick**: Navegación de cuatro direcciones (Arriba, Abajo, Izquierda, Derecha) más presión central
- **Key1 (A)**: Botón de acción principal
- **Key2 (B)**: Botón de acción secundario  
- **Key3 (C)**: Botón de acción terciario

### Referencia de Funciones de Botones

| Control        | Función                                    |
| -------------- | ------------------------------------------- |
| Joystick Arriba    | Mover selección hacia arriba                           |
| Joystick Abajo  | Mover selección hacia abajo                         |
| Joystick Izquierda  | Mover selección hacia la izquierda                         |
| Joystick Derecha | Mover selección hacia la derecha                        |
| Presión Joystick | Selección/confirmación alternativa (dependiente del contexto) |
| Key1 (A)       | Seleccionar opción resaltada o confirmar acción |
| Key2 (B)       | Seleccionar opción resaltada o confirmar acción |
| Key3 (C)       | Seleccionar opción resaltada o confirmar acción |

**Notas Importantes de Navegación**:

- Las tres teclas (A, B, C) funcionan de manera idéntica para selección y confirmación
- Para volver a una pantalla anterior, navega primero a la flecha/botón de retroceso usando el joystick, luego presiona cualquier tecla para activarlo
- La presión central del joystick puede tener diferentes funciones dependiendo del contexto de la pantalla actual

---

## 🏁 Conclusión

SeedSigner proporciona una solución segura y de código abierto para la gestión de claves de Bitcoin y la firma de transacciones. Siguiendo los flujos de trabajo de esta guía, puedes:

- ✅ Generar frases semilla verdaderamente aleatorias usando múltiples fuentes de entropía
- ✅ Cargar y gestionar de forma segura frases semilla existentes
- ✅ Firmar transacciones de Bitcoin sin exponer claves privadas a dispositivos conectados en red
- ✅ Exportar claves públicas para configuración de carteras de solo lectura
- ✅ Verificar la propiedad de direcciones y detalles de transacciones
- ✅ Mantener seguridad completa de separación de aire durante todas las operaciones

### Recuerda las Reglas de Oro

1. **Nunca omitas la verificación del respaldo de la semilla** - Una palabra incorrecta significa Bitcoin perdido
2. **Siempre verifica los detalles de la transacción** - Las transacciones de Bitcoin son irreversibles
3. **Mantén la seguridad de separación de aire** - Nunca conectes SeedSigner a redes
4. **Usa entornos privados** - Protégete contra vigilancia y grabación
5. **Almacena los respaldos de forma segura** - Trata las frases semilla como los activos valiosos que protegen

### Obtener Ayuda

Si encuentras problemas no cubiertos en esta guía:

- Revisa el repositorio oficial de SeedSigner en GitHub para actualizaciones
- Visita foros de la comunidad y grupos de chat para apoyo entre pares
- Revisa la sección de solución de problemas para soluciones comunes
- Considera contactar a la comunidad de desarrollo para problemas técnicos complejos

**Recuerda**: Tu seguridad de Bitcoin es en última instancia tu responsabilidad. Tómate el tiempo para entender cada paso, practica con cantidades pequeñas, y nunca te apresures durante operaciones críticas de seguridad.

---

*Esta guía es mantenida por la comunidad de SeedSigner y se actualiza regularmente. Para la versión más reciente y recursos adicionales, visita el repositorio oficial de SeedSigner en GitHub.*
