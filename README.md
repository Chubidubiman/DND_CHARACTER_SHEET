# D&D 5e Character Sheet

Hoja de personaje interactiva para Dungeons & Dragons 5ta Edicion, construida como una pagina HTML standalone.

## Caracteristicas

- **Universal**: Funciona para cualquier clase, raza o tipo de personaje de D&D 5e
- **Auto-calculos**: Modificadores de habilidad, bonus de proficiency, saving throws, skills, initiative, passive perception, spell save DC y spell attack se calculan automaticamente
- **Proficiency & Expertise**: Toggle de 3 estados en skills (sin proficiency, proficient, expertise) y proficiency en saving throws
- **Guardar/Cargar**: Exporta e importa la configuracion completa del personaje como archivo JSON
- **Nombre inteligente**: El archivo se nombra automaticamente como `Nombre-Clase.json` (ej: `Holong-Monk.json`)
- **Responsive**: Se adapta a pantallas de escritorio, tablet y celular
- **Spellcasting**: Seccion colapsable con slots por nivel (1-9) y cantrips
- **Sin dependencias**: Un solo archivo HTML, sin frameworks ni librerias externas

## Uso

1. Abrir `index.html` en cualquier navegador moderno
2. Llenar los datos del personaje
3. Hacer click en **Save Character** para descargar el archivo JSON
4. Hacer click en **Load Character** para restaurar un personaje guardado

## Secciones incluidas

| Seccion | Contenido |
|---|---|
| Info basica | Nombre, clase, nivel, raza, background, alignment, XP |
| Ability Scores | STR, DEX, CON, INT, WIS, CHA con modificadores automaticos |
| Saving Throws | 6 saves con toggle de proficiency |
| Skills | 18 skills con proficiency/expertise y ability tags |
| Combate | AC, initiative, speed, HP (max/current/temp), hit dice, death saves |
| Ataques | Tabla dinamica de armas/ataques (agregar/eliminar filas) |
| Personalidad | Traits, ideals, bonds, flaws |
| Equipo | Monedas (CP/SP/EP/GP/PP) y lista de equipo |
| Features & Traits | Rasgos raciales, features de clase, feats |
| Proficiencies | Armaduras, armas, herramientas, idiomas |
| Spellcasting | Clase, ability, DC, attack bonus, cantrips y niveles 1-9 con slots |
| Notas | Espacio libre para backstory, session log, etc. |

## Breakpoints responsive

- **Desktop** (>1100px): 3 columnas
- **Tablet landscape** (768-1100px): 2 columnas
- **Tablet portrait** (480-768px): 1 columna, padding reducido
- **Mobile** (<480px): Layout compacto, scroll horizontal en tabla de ataques

## Estructura del archivo JSON

```json
{
  "_version": "1.0",
  "charName": "Holong",
  "charClass": "Monk",
  "charLevel": "5",
  "ability_str": "14",
  "ability_dex": "18",
  "_profStates": {
    "save_prof_dex": 1,
    "skill_prof_stealth": 2
  },
  "_attacks": [
    { "name": "Unarmed Strike", "bonus": "+7", "damage": "1d6+4 bludgeoning" }
  ]
}
```

## Tecnologias

- HTML5
- CSS3 (Grid, Flexbox, Custom Properties)
- JavaScript vanilla (ES6+)
