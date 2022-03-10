# Tresure Hunt

A digger inspired multiplayer game using Phaser 3 and Nakama

## Requirements

[Node.js](https://nodejs.org) is required to install dependencies and run scripts via `npm`.

## Available Commands

| Command | Description |
|---------|-------------|
| `npm install` | Install project dependencies |
| `npm dev` | Build project and open web server running project |
| `npm run build` | Builds code bundle with production settings (minification, uglification, etc..) |

## Writing Code

After cloning the repo, run `npm install` from your project directory. Then, you can start the local development
server by running `npm dev`.


After starting the development server with `npm dev`, you can edit any files in the `src` folder
and webpack will automatically recompile and reload your server (available at `http://localhost:8080`
by default).

## Customizing Template

### Babel
You can write modern ES6+ JavaScript and Babel will transpile it to a version of JavaScript that you
want your project to support. The targeted browsers are set in the `.babelrc` file and the default currently
targets all browsers with total usage over "0.25%" but excludes IE11 and Opera Mini.

  ```
  "browsers": [
    ">0.25%",
    "not ie 11",
    "not op_mini all"
  ]
  ```

### Webpack
If you want to customize your build, such as adding a new webpack loader or plugin (i.e. for loading CSS or fonts), you can
modify the `webpack/base.js` file for cross-project changes, or you can modify and/or create
new configuration files and target them in specific npm tasks inside of `package.json'.

## Deploying Code
After you run the `npm run build` command, your code will be built into a single bundle located at
`dist/bundle.min.js` along with any other assets you project depended.

If you put the contents of the `dist` folder in a publicly-accessible location (say something like `http://treasurehunt.com`),
you should be able to open `http://treasurehunt.com/index.html` and play your game.

```
treasurehunt-master
├─ .babelrc
├─ .gitignore
├─ index.html
├─ LICENSE
├─ nakama
│  ├─ .cookie
│  ├─ docker-compose.yml
│  └─ modules
├─ package-lock.json
├─ package.json
├─ README.md
├─ src
│  ├─ assets
│  │  ├─ atlas.json
│  │  ├─ atlas.png
│  │  ├─ fonts
│  │  │  ├─ CelticTime12.png
│  │  │  └─ CelticTime12.xml
│  │  ├─ logo.png
│  │  ├─ source
│  │  │  ├─ 0x72_DungeonTileset_v1
│  │  │  │  ├─ big_demon_idle_anim_f0.png
│  │  │  │  ├─ big_demon_idle_anim_f1.png
│  │  │  │  ├─ big_demon_idle_anim_f2.png
│  │  │  │  ├─ big_demon_idle_anim_f3.png
│  │  │  │  ├─ big_demon_run_anim_f0.png
│  │  │  │  ├─ big_demon_run_anim_f1.png
│  │  │  │  ├─ big_demon_run_anim_f2.png
│  │  │  │  ├─ big_demon_run_anim_f3.png
│  │  │  │  ├─ big_zombie_idle_anim_f0.png
│  │  │  │  ├─ big_zombie_idle_anim_f1.png
│  │  │  │  ├─ big_zombie_idle_anim_f2.png
│  │  │  │  ├─ big_zombie_idle_anim_f3.png
│  │  │  │  ├─ big_zombie_run_anim_f0.png
│  │  │  │  ├─ big_zombie_run_anim_f1.png
│  │  │  │  ├─ big_zombie_run_anim_f2.png
│  │  │  │  ├─ big_zombie_run_anim_f3.png
│  │  │  │  ├─ chest_empty_open_anim_f0.png
│  │  │  │  ├─ chest_empty_open_anim_f1.png
│  │  │  │  ├─ chest_empty_open_anim_f2.png
│  │  │  │  ├─ chest_full_open_anim_f0.png
│  │  │  │  ├─ chest_full_open_anim_f1.png
│  │  │  │  ├─ chest_full_open_anim_f2.png
│  │  │  │  ├─ chest_mimic_open_anim_f0.png
│  │  │  │  ├─ chest_mimic_open_anim_f1.png
│  │  │  │  ├─ chest_mimic_open_anim_f2.png
│  │  │  │  ├─ chort_idle_anim_f0.png
│  │  │  │  ├─ chort_idle_anim_f1.png
│  │  │  │  ├─ chort_idle_anim_f2.png
│  │  │  │  ├─ chort_idle_anim_f3.png
│  │  │  │  ├─ chort_run_anim_f0.png
│  │  │  │  ├─ chort_run_anim_f1.png
│  │  │  │  ├─ chort_run_anim_f2.png
│  │  │  │  ├─ chort_run_anim_f3.png
│  │  │  │  ├─ coin_anim_f0.png
│  │  │  │  ├─ coin_anim_f1.png
│  │  │  │  ├─ coin_anim_f2.png
│  │  │  │  ├─ coin_anim_f3.png
│  │  │  │  ├─ column_mid.png
│  │  │  │  ├─ column_top.png
│  │  │  │  ├─ coulmn_base.png
│  │  │  │  ├─ crate.png
│  │  │  │  ├─ doors_all.png
│  │  │  │  ├─ doors_frame_left.png
│  │  │  │  ├─ doors_frame_righ.png
│  │  │  │  ├─ doors_frame_top.png
│  │  │  │  ├─ doors_leaf_closed.png
│  │  │  │  ├─ doors_leaf_open.png
│  │  │  │  ├─ edge.png
│  │  │  │  ├─ elf_f_hit_anim_f0.png
│  │  │  │  ├─ elf_f_idle_anim_f0.png
│  │  │  │  ├─ elf_f_idle_anim_f1.png
│  │  │  │  ├─ elf_f_idle_anim_f2.png
│  │  │  │  ├─ elf_f_idle_anim_f3.png
│  │  │  │  ├─ elf_f_run_anim_f0.png
│  │  │  │  ├─ elf_f_run_anim_f1.png
│  │  │  │  ├─ elf_f_run_anim_f2.png
│  │  │  │  ├─ elf_f_run_anim_f3.png
│  │  │  │  ├─ elf_m_hit_anim_f0.png
│  │  │  │  ├─ elf_m_idle_anim_f0.png
│  │  │  │  ├─ elf_m_idle_anim_f1.png
│  │  │  │  ├─ elf_m_idle_anim_f2.png
│  │  │  │  ├─ elf_m_idle_anim_f3.png
│  │  │  │  ├─ elf_m_run_anim_f0.png
│  │  │  │  ├─ elf_m_run_anim_f1.png
│  │  │  │  ├─ elf_m_run_anim_f2.png
│  │  │  │  ├─ elf_m_run_anim_f3.png
│  │  │  │  ├─ flask_big_blue.png
│  │  │  │  ├─ flask_big_green.png
│  │  │  │  ├─ flask_big_red.png
│  │  │  │  ├─ flask_big_yellow.png
│  │  │  │  ├─ flask_blue.png
│  │  │  │  ├─ flask_green.png
│  │  │  │  ├─ flask_red.png
│  │  │  │  ├─ flask_yellow.png
│  │  │  │  ├─ floor_1.png
│  │  │  │  ├─ floor_2.png
│  │  │  │  ├─ floor_3.png
│  │  │  │  ├─ floor_4.png
│  │  │  │  ├─ floor_5.png
│  │  │  │  ├─ floor_6.png
│  │  │  │  ├─ floor_7.png
│  │  │  │  ├─ floor_8.png
│  │  │  │  ├─ floor_ladder.png
│  │  │  │  ├─ floor_spikes_anim_f0.png
│  │  │  │  ├─ floor_spikes_anim_f1.png
│  │  │  │  ├─ floor_spikes_anim_f2.png
│  │  │  │  ├─ floor_spikes_anim_f3.png
│  │  │  │  ├─ goblin_idle_anim_f0.png
│  │  │  │  ├─ goblin_idle_anim_f1.png
│  │  │  │  ├─ goblin_idle_anim_f2.png
│  │  │  │  ├─ goblin_idle_anim_f3.png
│  │  │  │  ├─ goblin_run_anim_f0.png
│  │  │  │  ├─ goblin_run_anim_f1.png
│  │  │  │  ├─ goblin_run_anim_f2.png
│  │  │  │  ├─ goblin_run_anim_f3.png
│  │  │  │  ├─ hole.png
│  │  │  │  ├─ ice_zombie_idle_anim_f0.png
│  │  │  │  ├─ ice_zombie_idle_anim_f1.png
│  │  │  │  ├─ ice_zombie_idle_anim_f2.png
│  │  │  │  ├─ ice_zombie_idle_anim_f3.png
│  │  │  │  ├─ ice_zombie_run_anim_f0.png
│  │  │  │  ├─ ice_zombie_run_anim_f1.png
│  │  │  │  ├─ ice_zombie_run_anim_f2.png
│  │  │  │  ├─ ice_zombie_run_anim_f3.png
│  │  │  │  ├─ imp_idle_anim_f0.png
│  │  │  │  ├─ imp_idle_anim_f1.png
│  │  │  │  ├─ imp_idle_anim_f2.png
│  │  │  │  ├─ imp_idle_anim_f3.png
│  │  │  │  ├─ imp_run_anim_f0.png
│  │  │  │  ├─ imp_run_anim_f1.png
│  │  │  │  ├─ imp_run_anim_f2.png
│  │  │  │  ├─ imp_run_anim_f3.png
│  │  │  │  ├─ knight_f_hit_anim_f0.png
│  │  │  │  ├─ knight_f_idle_anim_f0.png
│  │  │  │  ├─ knight_f_idle_anim_f1.png
│  │  │  │  ├─ knight_f_idle_anim_f2.png
│  │  │  │  ├─ knight_f_idle_anim_f3.png
│  │  │  │  ├─ knight_f_run_anim_f0.png
│  │  │  │  ├─ knight_f_run_anim_f1.png
│  │  │  │  ├─ knight_f_run_anim_f2.png
│  │  │  │  ├─ knight_f_run_anim_f3.png
│  │  │  │  ├─ knight_m_hit_anim_f0.png
│  │  │  │  ├─ knight_m_idle_anim_f0.png
│  │  │  │  ├─ knight_m_idle_anim_f1.png
│  │  │  │  ├─ knight_m_idle_anim_f2.png
│  │  │  │  ├─ knight_m_idle_anim_f3.png
│  │  │  │  ├─ knight_m_run_anim_f0.png
│  │  │  │  ├─ knight_m_run_anim_f1.png
│  │  │  │  ├─ knight_m_run_anim_f2.png
│  │  │  │  ├─ knight_m_run_anim_f3.png
│  │  │  │  ├─ masked_orc_idle_anim_f0.png
│  │  │  │  ├─ masked_orc_idle_anim_f1.png
│  │  │  │  ├─ masked_orc_idle_anim_f2.png
│  │  │  │  ├─ masked_orc_idle_anim_f3.png
│  │  │  │  ├─ masked_orc_run_anim_f0.png
│  │  │  │  ├─ masked_orc_run_anim_f1.png
│  │  │  │  ├─ masked_orc_run_anim_f2.png
│  │  │  │  ├─ masked_orc_run_anim_f3.png
│  │  │  │  ├─ muddy_idle_anim_f0.png
│  │  │  │  ├─ muddy_idle_anim_f1.png
│  │  │  │  ├─ muddy_idle_anim_f2.png
│  │  │  │  ├─ muddy_idle_anim_f3.png
│  │  │  │  ├─ muddy_run_anim_f0.png
│  │  │  │  ├─ muddy_run_anim_f1.png
│  │  │  │  ├─ muddy_run_anim_f2.png
│  │  │  │  ├─ muddy_run_anim_f3.png
│  │  │  │  ├─ necromancer_idle_anim_f0.png
│  │  │  │  ├─ necromancer_idle_anim_f1.png
│  │  │  │  ├─ necromancer_idle_anim_f2.png
│  │  │  │  ├─ necromancer_idle_anim_f3.png
│  │  │  │  ├─ necromancer_run_anim_f0.png
│  │  │  │  ├─ necromancer_run_anim_f1.png
│  │  │  │  ├─ necromancer_run_anim_f2.png
│  │  │  │  ├─ necromancer_run_anim_f3.png
│  │  │  │  ├─ ogre_idle_anim_f0.png
│  │  │  │  ├─ ogre_idle_anim_f1.png
│  │  │  │  ├─ ogre_idle_anim_f2.png
│  │  │  │  ├─ ogre_idle_anim_f3.png
│  │  │  │  ├─ ogre_run_anim_f0.png
│  │  │  │  ├─ ogre_run_anim_f1.png
│  │  │  │  ├─ ogre_run_anim_f2.png
│  │  │  │  ├─ ogre_run_anim_f3.png
│  │  │  │  ├─ orc_shaman_idle_anim_f0.png
│  │  │  │  ├─ orc_shaman_idle_anim_f1.png
│  │  │  │  ├─ orc_shaman_idle_anim_f2.png
│  │  │  │  ├─ orc_shaman_idle_anim_f3.png
│  │  │  │  ├─ orc_shaman_run_anim_f0.png
│  │  │  │  ├─ orc_shaman_run_anim_f1.png
│  │  │  │  ├─ orc_shaman_run_anim_f2.png
│  │  │  │  ├─ orc_shaman_run_anim_f3.png
│  │  │  │  ├─ orc_warrior_idle_anim_f0.png
│  │  │  │  ├─ orc_warrior_idle_anim_f1.png
│  │  │  │  ├─ orc_warrior_idle_anim_f2.png
│  │  │  │  ├─ orc_warrior_idle_anim_f3.png
│  │  │  │  ├─ orc_warrior_run_anim_f0.png
│  │  │  │  ├─ orc_warrior_run_anim_f1.png
│  │  │  │  ├─ orc_warrior_run_anim_f2.png
│  │  │  │  ├─ orc_warrior_run_anim_f3.png
│  │  │  │  ├─ skelet_idle_anim_f0.png
│  │  │  │  ├─ skelet_idle_anim_f1.png
│  │  │  │  ├─ skelet_idle_anim_f2.png
│  │  │  │  ├─ skelet_idle_anim_f3.png
│  │  │  │  ├─ skelet_run_anim_f0.png
│  │  │  │  ├─ skelet_run_anim_f1.png
│  │  │  │  ├─ skelet_run_anim_f2.png
│  │  │  │  ├─ skelet_run_anim_f3.png
│  │  │  │  ├─ skull.png
│  │  │  │  ├─ swampy_idle_anim_f0.png
│  │  │  │  ├─ swampy_idle_anim_f1.png
│  │  │  │  ├─ swampy_idle_anim_f2.png
│  │  │  │  ├─ swampy_idle_anim_f3.png
│  │  │  │  ├─ swampy_run_anim_f0.png
│  │  │  │  ├─ swampy_run_anim_f1.png
│  │  │  │  ├─ swampy_run_anim_f2.png
│  │  │  │  ├─ swampy_run_anim_f3.png
│  │  │  │  ├─ tiles_list_v1.1
│  │  │  │  ├─ tiny_zombie_idle_anim_f0.png
│  │  │  │  ├─ tiny_zombie_idle_anim_f1.png
│  │  │  │  ├─ tiny_zombie_idle_anim_f2.png
│  │  │  │  ├─ tiny_zombie_idle_anim_f3.png
│  │  │  │  ├─ tiny_zombie_run_anim_f0.png
│  │  │  │  ├─ tiny_zombie_run_anim_f1.png
│  │  │  │  ├─ tiny_zombie_run_anim_f2.png
│  │  │  │  ├─ tiny_zombie_run_anim_f3.png
│  │  │  │  ├─ ui_heart_empty.png
│  │  │  │  ├─ ui_heart_full.png
│  │  │  │  ├─ ui_heart_half.png
│  │  │  │  ├─ wall_banner_blue.png
│  │  │  │  ├─ wall_banner_green.png
│  │  │  │  ├─ wall_banner_red.png
│  │  │  │  ├─ wall_banner_yellow.png
│  │  │  │  ├─ wall_column_mid.png
│  │  │  │  ├─ wall_column_top.png
│  │  │  │  ├─ wall_corner_bottom_left.png
│  │  │  │  ├─ wall_corner_bottom_right.png
│  │  │  │  ├─ wall_corner_front_left.png
│  │  │  │  ├─ wall_corner_front_right.png
│  │  │  │  ├─ wall_corner_left.png
│  │  │  │  ├─ wall_corner_right.png
│  │  │  │  ├─ wall_corner_top_left.png
│  │  │  │  ├─ wall_corner_top_right.png
│  │  │  │  ├─ wall_coulmn_base.png
│  │  │  │  ├─ wall_fountain_basin_blue_anim_f0.png
│  │  │  │  ├─ wall_fountain_basin_blue_anim_f1.png
│  │  │  │  ├─ wall_fountain_basin_blue_anim_f2.png
│  │  │  │  ├─ wall_fountain_basin_red_anim_f0.png
│  │  │  │  ├─ wall_fountain_basin_red_anim_f1.png
│  │  │  │  ├─ wall_fountain_basin_red_anim_f2.png
│  │  │  │  ├─ wall_fountain_mid_blue_anim_f0.png
│  │  │  │  ├─ wall_fountain_mid_blue_anim_f1.png
│  │  │  │  ├─ wall_fountain_mid_blue_anim_f2.png
│  │  │  │  ├─ wall_fountain_mid_red_anim_f0.png
│  │  │  │  ├─ wall_fountain_mid_red_anim_f1.png
│  │  │  │  ├─ wall_fountain_mid_red_anim_f2.png
│  │  │  │  ├─ wall_fountain_top.png
│  │  │  │  ├─ wall_goo.png
│  │  │  │  ├─ wall_goo_base.png
│  │  │  │  ├─ wall_hole_1.png
│  │  │  │  ├─ wall_hole_2.png
│  │  │  │  ├─ wall_inner_corner_l_top_left.png
│  │  │  │  ├─ wall_inner_corner_l_top_rigth.png
│  │  │  │  ├─ wall_inner_corner_mid_left.png
│  │  │  │  ├─ wall_inner_corner_mid_rigth.png
│  │  │  │  ├─ wall_inner_corner_t_top_left.png
│  │  │  │  ├─ wall_inner_corner_t_top_rigth.png
│  │  │  │  ├─ wall_left.png
│  │  │  │  ├─ wall_mid.png
│  │  │  │  ├─ wall_right.png
│  │  │  │  ├─ wall_side_front_left.png
│  │  │  │  ├─ wall_side_front_right.png
│  │  │  │  ├─ wall_side_mid_left.png
│  │  │  │  ├─ wall_side_mid_right.png
│  │  │  │  ├─ wall_side_top_left.png
│  │  │  │  ├─ wall_side_top_right.png
│  │  │  │  ├─ wall_top_left.png
│  │  │  │  ├─ wall_top_mid.png
│  │  │  │  ├─ wall_top_right.png
│  │  │  │  ├─ weapon_anime_sword.png
│  │  │  │  ├─ weapon_axe.png
│  │  │  │  ├─ weapon_baton_with_spikes.png
│  │  │  │  ├─ weapon_big_hammer.png
│  │  │  │  ├─ weapon_cleaver.png
│  │  │  │  ├─ weapon_duel_sword.png
│  │  │  │  ├─ weapon_golden_sword.png
│  │  │  │  ├─ weapon_green_magic_staff.png
│  │  │  │  ├─ weapon_hammer.png
│  │  │  │  ├─ weapon_katana.png
│  │  │  │  ├─ weapon_knife.png
│  │  │  │  ├─ weapon_knight_sword.png
│  │  │  │  ├─ weapon_lavish_sword.png
│  │  │  │  ├─ weapon_mace.png
│  │  │  │  ├─ weapon_machete.png
│  │  │  │  ├─ weapon_red_gem_sword.png
│  │  │  │  ├─ weapon_red_magic_staff.png
│  │  │  │  ├─ weapon_regular_sword.png
│  │  │  │  ├─ weapon_rusty_sword.png
│  │  │  │  ├─ weapon_saw_sword.png
│  │  │  │  ├─ wizzard_f_idle_anim_f0.png
│  │  │  │  ├─ wizzard_f_idle_anim_f1.png
│  │  │  │  ├─ wizzard_f_idle_anim_f2.png
│  │  │  │  ├─ wizzard_f_idle_anim_f3.png
│  │  │  │  ├─ wizzard_m_idle_anim_f0.png
│  │  │  │  ├─ wizzard_m_idle_anim_f1.png
│  │  │  │  ├─ wizzard_m_idle_anim_f2.png
│  │  │  │  ├─ wizzard_m_idle_anim_f3.png
│  │  │  │  ├─ wizzart_f_hit_anim_f0.png
│  │  │  │  ├─ wizzart_f_run_anim_f0.png
│  │  │  │  ├─ wizzart_f_run_anim_f1.png
│  │  │  │  ├─ wizzart_f_run_anim_f2.png
│  │  │  │  ├─ wizzart_f_run_anim_f3.png
│  │  │  │  ├─ wizzart_m_hit_anim_f0.png
│  │  │  │  ├─ wizzart_m_run_anim_f0.png
│  │  │  │  ├─ wizzart_m_run_anim_f1.png
│  │  │  │  ├─ wizzart_m_run_anim_f2.png
│  │  │  │  ├─ wizzart_m_run_anim_f3.png
│  │  │  │  ├─ wogol_idle_anim_f0.png
│  │  │  │  ├─ wogol_idle_anim_f1.png
│  │  │  │  ├─ wogol_idle_anim_f2.png
│  │  │  │  ├─ wogol_idle_anim_f3.png
│  │  │  │  ├─ wogol_run_anim_f0.png
│  │  │  │  ├─ wogol_run_anim_f1.png
│  │  │  │  ├─ wogol_run_anim_f2.png
│  │  │  │  ├─ wogol_run_anim_f3.png
│  │  │  │  ├─ zombie_idle_anim_f0.png
│  │  │  │  ├─ zombie_idle_anim_f1.png
│  │  │  │  ├─ zombie_idle_anim_f2.png
│  │  │  │  ├─ zombie_idle_anim_f3.png
│  │  │  │  ├─ zombie_run_anim_f0.png
│  │  │  │  ├─ zombie_run_anim_f1.png
│  │  │  │  ├─ zombie_run_anim_f2.png
│  │  │  │  └─ zombie_run_anim_f3.png
│  │  │  ├─ atlas.tps
│  │  │  ├─ Mine_Tileset
│  │  │  │  ├─ background.png
│  │  │  │  ├─ spr_alert_black_0.png
│  │  │  │  ├─ spr_alert_red_0.png
│  │  │  │  ├─ spr_blade_0.png
│  │  │  │  ├─ spr_blue_gem_0.png
│  │  │  │  ├─ spr_boss_black_0.png
│  │  │  │  ├─ spr_boss_red_0.png
│  │  │  │  ├─ spr_box_0.png
│  │  │  │  ├─ spr_box_big_0.png
│  │  │  │  ├─ spr_box_small_0.png
│  │  │  │  ├─ spr_bridge_0.png
│  │  │  │  ├─ spr_cart_0.png
│  │  │  │  ├─ spr_chest_0.png
│  │  │  │  ├─ spr_down_black_0.png
│  │  │  │  ├─ spr_down_red_0.png
│  │  │  │  ├─ spr_green_gem_0.png
│  │  │  │  ├─ spr_ground_bottom_7_0.png
│  │  │  │  ├─ spr_ground_bottom_8_0.png
│  │  │  │  ├─ spr_ground_bottom_left_3_0.png
│  │  │  │  ├─ spr_ground_bottom_left_5_0.png
│  │  │  │  ├─ spr_ground_bottom_left_right_1_0.png
│  │  │  │  ├─ spr_ground_bottom_left_right_2_0.png
│  │  │  │  ├─ spr_ground_bottom_right_4_0.png
│  │  │  │  ├─ spr_ground_bottom_right_6_0.png
│  │  │  │  ├─ spr_ground_center_10_0.png
│  │  │  │  ├─ spr_ground_center_11_0.png
│  │  │  │  ├─ spr_ground_center_12_0.png
│  │  │  │  ├─ spr_ground_center_13_0.png
│  │  │  │  ├─ spr_ground_center_14_0.png
│  │  │  │  ├─ spr_ground_center_15_0.png
│  │  │  │  ├─ spr_ground_center_16_0.png
│  │  │  │  ├─ spr_ground_center_17_0.png
│  │  │  │  ├─ spr_ground_center_1_0.png
│  │  │  │  ├─ spr_ground_center_2_0.png
│  │  │  │  ├─ spr_ground_center_3_0.png
│  │  │  │  ├─ spr_ground_center_4_0.png
│  │  │  │  ├─ spr_ground_center_5_0.png
│  │  │  │  ├─ spr_ground_center_6_0.png
│  │  │  │  ├─ spr_ground_center_7_0.png
│  │  │  │  ├─ spr_ground_center_8_0.png
│  │  │  │  ├─ spr_ground_center_9_0.png
│  │  │  │  ├─ spr_ground_left_10_0.png
│  │  │  │  ├─ spr_ground_left_11_0.png
│  │  │  │  ├─ spr_ground_left_12_0.png
│  │  │  │  ├─ spr_ground_left_1_0.png
│  │  │  │  ├─ spr_ground_left_2_0.png
│  │  │  │  ├─ spr_ground_left_3_0.png
│  │  │  │  ├─ spr_ground_left_4_0.png
│  │  │  │  ├─ spr_ground_left_5_0.png
│  │  │  │  ├─ spr_ground_left_6_0.png
│  │  │  │  ├─ spr_ground_left_7_0.png
│  │  │  │  ├─ spr_ground_left_8_0.png
│  │  │  │  ├─ spr_ground_left_9_0.png
│  │  │  │  ├─ spr_ground_right_10_0.png
│  │  │  │  ├─ spr_ground_right_11_0.png
│  │  │  │  ├─ spr_ground_right_12_0.png
│  │  │  │  ├─ spr_ground_right_1_0.png
│  │  │  │  ├─ spr_ground_right_2_0.png
│  │  │  │  ├─ spr_ground_right_3_0.png
│  │  │  │  ├─ spr_ground_right_4_0.png
│  │  │  │  ├─ spr_ground_right_5_0.png
│  │  │  │  ├─ spr_ground_right_6_0.png
│  │  │  │  ├─ spr_ground_right_7_0.png
│  │  │  │  ├─ spr_ground_right_8_0.png
│  │  │  │  ├─ spr_ground_right_9_0.png
│  │  │  │  ├─ spr_left_black_0.png
│  │  │  │  ├─ spr_left_red_0.png
│  │  │  │  ├─ spr_red_gem_0.png
│  │  │  │  ├─ spr_right_black_0.png
│  │  │  │  ├─ spr_right_red_0.png
│  │  │  │  ├─ spr_staircase_0.png
│  │  │  │  ├─ spr_thorns_0.png
│  │  │  │  ├─ spr_up_black_0.png
│  │  │  │  └─ spr_up_red_0.png
│  │  │  ├─ Mining-Gfx
│  │  │  │  ├─ AtlasSingle
│  │  │  │  │  ├─ action
│  │  │  │  │  │  ├─ action_dwarf.png
│  │  │  │  │  │  ├─ action_opendoor.png
│  │  │  │  │  │  ├─ action_remove_ladder.png
│  │  │  │  │  │  ├─ action_save.png
│  │  │  │  │  │  ├─ action_uselift0.png
│  │  │  │  │  │  ├─ action_uselift1.png
│  │  │  │  │  │  ├─ depar_bag.png
│  │  │  │  │  │  ├─ depar_ladder.png
│  │  │  │  │  │  ├─ depar_material.png
│  │  │  │  │  │  ├─ enpar_bag.png
│  │  │  │  │  │  ├─ enpar_ladder.png
│  │  │  │  │  │  └─ enpar_material.png
│  │  │  │  │  ├─ actor
│  │  │  │  │  │  ├─ cm-r-climb_1.png
│  │  │  │  │  │  ├─ cm-r-climb_2.png
│  │  │  │  │  │  ├─ cm-r-climb_3.png
│  │  │  │  │  │  ├─ cm-r-climb_4.png
│  │  │  │  │  │  ├─ cm-r-dig_1.png
│  │  │  │  │  │  ├─ cm-r-dig_2.png
│  │  │  │  │  │  ├─ cm-r-drill_1.png
│  │  │  │  │  │  ├─ cm-r-drill_2.png
│  │  │  │  │  │  ├─ cm-r-drill_down_1.png
│  │  │  │  │  │  ├─ cm-r-drill_down_2.png
│  │  │  │  │  │  ├─ cm-r-drill_up_1.png
│  │  │  │  │  │  ├─ cm-r-drill_up_2.png
│  │  │  │  │  │  ├─ cm-r-fall_1.png
│  │  │  │  │  │  ├─ cm-r-fall_2.png
│  │  │  │  │  │  ├─ cm-r-gpick_1.png
│  │  │  │  │  │  ├─ cm-r-gpick_2.png
│  │  │  │  │  │  ├─ cm-r-jetpack_1.png
│  │  │  │  │  │  ├─ cm-r-jetpack_2.png
│  │  │  │  │  │  ├─ cm-r-jetpack_3.png
│  │  │  │  │  │  ├─ cm-r-jetpack_4.png
│  │  │  │  │  │  ├─ cm-r-lift_1.png
│  │  │  │  │  │  ├─ cm-r-lift_2.png
│  │  │  │  │  │  ├─ cm-r-pick_1.png
│  │  │  │  │  │  ├─ cm-r-pick_2.png
│  │  │  │  │  │  ├─ cm-r-saber_1.png
│  │  │  │  │  │  ├─ cm-r-saber_2.png
│  │  │  │  │  │  ├─ cm-r-walk_1.png
│  │  │  │  │  │  ├─ cm-r-walk_2.png
│  │  │  │  │  │  ├─ cm-r-walk_3.png
│  │  │  │  │  │  ├─ cm-r-walk_4.png
│  │  │  │  │  │  ├─ cm-r-wink_1.png
│  │  │  │  │  │  ├─ cm-r-wink_2.png
│  │  │  │  │  │  ├─ cm-r-wink_3.png
│  │  │  │  │  │  ├─ cm-r-wink_4.png
│  │  │  │  │  │  ├─ pl_die.png
│  │  │  │  │  │  ├─ Skin ABC
│  │  │  │  │  │  │  ├─ ABC.ase
│  │  │  │  │  │  │  ├─ ABC.png
│  │  │  │  │  │  │  ├─ Gehen
│  │  │  │  │  │  │  │  ├─ ABC-gehen1.png
│  │  │  │  │  │  │  │  ├─ ABC-gehen2.png
│  │  │  │  │  │  │  │  └─ ABC-gehen3.png
│  │  │  │  │  │  │  ├─ Jetpack
│  │  │  │  │  │  │  │  ├─ jetpack1.ase
│  │  │  │  │  │  │  │  ├─ jetpack1.png
│  │  │  │  │  │  │  │  └─ jetpack2.png
│  │  │  │  │  │  │  ├─ Klettern
│  │  │  │  │  │  │  │  ├─ 111cm-r-climb_1.ase
│  │  │  │  │  │  │  │  ├─ cm-r-climb_1.ase
│  │  │  │  │  │  │  │  ├─ klettern1.png
│  │  │  │  │  │  │  │  ├─ klettern2.png
│  │  │  │  │  │  │  │  └─ klettern3.png
│  │  │  │  │  │  │  ├─ Picke
│  │  │  │  │  │  │  │  ├─ ABC-picke.ase
│  │  │  │  │  │  │  │  ├─ ABC-picke1.png
│  │  │  │  │  │  │  │  └─ ABC-picke2.png
│  │  │  │  │  │  │  └─ Sterbe
│  │  │  │  │  │  │     ├─ die.ase
│  │  │  │  │  │  │     └─ die.png
│  │  │  │  │  │  └─ Skin Sauerstoff
│  │  │  │  │  │     ├─ cm-r-climb_1.png
│  │  │  │  │  │     ├─ cm-r-climb_2.png
│  │  │  │  │  │     ├─ cm-r-climb_3.png
│  │  │  │  │  │     ├─ cm-r-climb_4.png
│  │  │  │  │  │     ├─ cm-r-drill_1.png
│  │  │  │  │  │     ├─ cm-r-drill_2.png
│  │  │  │  │  │     ├─ cm-r-drill_down_1.png
│  │  │  │  │  │     ├─ cm-r-drill_down_2.png
│  │  │  │  │  │     ├─ cm-r-drill_up_1.png
│  │  │  │  │  │     ├─ cm-r-drill_up_2.png
│  │  │  │  │  │     ├─ cm-r-pick_1.png
│  │  │  │  │  │     ├─ cm-r-pick_2.png
│  │  │  │  │  │     ├─ cm-r-walk_1.png
│  │  │  │  │  │     ├─ cm-r-walk_2.png
│  │  │  │  │  │     ├─ cm-r-walk_3.png
│  │  │  │  │  │     ├─ cm-r-walk_4.png
│  │  │  │  │  │     ├─ Fallen
│  │  │  │  │  │     │  ├─ fallen1.png
│  │  │  │  │  │     │  └─ fallen2.png
│  │  │  │  │  │     ├─ fallen.ase
│  │  │  │  │  │     ├─ Goldene Picke
│  │  │  │  │  │     │  ├─ GoldenePicke1.png
│  │  │  │  │  │     │  └─ GoldenePicke2.png
│  │  │  │  │  │     ├─ GoldenePicke.ase
│  │  │  │  │  │     ├─ Jetpack
│  │  │  │  │  │     │  ├─ jetpack1.png
│  │  │  │  │  │     │  ├─ jetpack2.png
│  │  │  │  │  │     │  ├─ jetpack3.png
│  │  │  │  │  │     │  └─ jetpack4.png
│  │  │  │  │  │     ├─ jetpack.ase
│  │  │  │  │  │     ├─ Schaufel
│  │  │  │  │  │     │  ├─ schaufel1.png
│  │  │  │  │  │     │  └─ schaufel2.png
│  │  │  │  │  │     ├─ schaufel.ase
│  │  │  │  │  │     └─ Sterbeanimation
│  │  │  │  │  │        └─ die.png
│  │  │  │  │  ├─ air_wheel.png
│  │  │  │  │  ├─ background
│  │  │  │  │  │  ├─ background.png
│  │  │  │  │  │  ├─ lb-px-background_forest1.png
│  │  │  │  │  │  ├─ lb-px-background_forest2.png
│  │  │  │  │  │  ├─ lb-px-background_gras1.png
│  │  │  │  │  │  ├─ lb-px-background_gras2.png
│  │  │  │  │  │  ├─ lb-px-background_hill1.png
│  │  │  │  │  │  ├─ lb-px-background_hill2.png
│  │  │  │  │  │  ├─ lb-px-cloud_1.png
│  │  │  │  │  │  ├─ lb-px-cloud_2.png
│  │  │  │  │  │  ├─ lb-px-cloud_3.png
│  │  │  │  │  │  └─ lb-px-cloud_4.png
│  │  │  │  │  ├─ background_shop.png
│  │  │  │  │  ├─ bg_company.png
│  │  │  │  │  ├─ bg_info1.png
│  │  │  │  │  ├─ btn1_company.png
│  │  │  │  │  ├─ btn2_company.png
│  │  │  │  │  ├─ btn3_company.png
│  │  │  │  │  ├─ btn_256off.png
│  │  │  │  │  ├─ btn_256on.png
│  │  │  │  │  ├─ btn_decrease.png
│  │  │  │  │  ├─ btn_increase.png
│  │  │  │  │  ├─ company_mineinc.png
│  │  │  │  │  ├─ company_rocketinc.png
│  │  │  │  │  ├─ controll
│  │  │  │  │  │  ├─ gamebutton.png
│  │  │  │  │  │  ├─ gamebutton2.png
│  │  │  │  │  │  ├─ gamebutton3.png
│  │  │  │  │  │  ├─ gamebutton3active.png
│  │  │  │  │  │  ├─ gamebutton3tool.png
│  │  │  │  │  │  ├─ gamepad.png
│  │  │  │  │  │  ├─ gamepad2.png
│  │  │  │  │  │  └─ gamepad_push.png
│  │  │  │  │  ├─ dwarf
│  │  │  │  │  │  ├─ lb-r-dwarfmain.png
│  │  │  │  │  │  ├─ lb-r-dwarf_idle1.png
│  │  │  │  │  │  ├─ lb-r-dwarf_idle2.png
│  │  │  │  │  │  ├─ lb-r-dwarf_idle3.png
│  │  │  │  │  │  ├─ lb-r-dwarf_lamp1.png
│  │  │  │  │  │  ├─ lb-r-dwarf_lamp2.png
│  │  │  │  │  │  ├─ lb-r-dwarf_lampon1.png
│  │  │  │  │  │  ├─ lb-r-dwarf_lampon2.png
│  │  │  │  │  │  ├─ lb-r-dwarf_stand.png
│  │  │  │  │  │  ├─ lb-r-dwarf_tent1.png
│  │  │  │  │  │  ├─ lb-r-dwarf_tent2.png
│  │  │  │  │  │  ├─ lb-r-dwarf_tent3.png
│  │  │  │  │  │  ├─ lb-r-dwarf_tent4.png
│  │  │  │  │  │  ├─ lb-r-dwarf_tent5.png
│  │  │  │  │  │  ├─ lb-r-dwarf_tent5a.png
│  │  │  │  │  │  ├─ lb-r-dwarf_tent6.png
│  │  │  │  │  │  ├─ lb-r-dwarf_tent6a.png
│  │  │  │  │  │  ├─ lb-r-dwarf_tent7.png
│  │  │  │  │  │  └─ lb-r-dwarf_tent7a.png
│  │  │  │  │  ├─ flag_england.png
│  │  │  │  │  ├─ flag_germany.png
│  │  │  │  │  ├─ gui_code.png
│  │  │  │  │  ├─ gui_restore.png
│  │  │  │  │  ├─ gui_soundoff.png
│  │  │  │  │  ├─ gui_soundon.png
│  │  │  │  │  ├─ home
│  │  │  │  │  │  ├─ lb-r-home.png
│  │  │  │  │  │  ├─ lb-r-home_ani1.png
│  │  │  │  │  │  ├─ lb-r-home_cloud1.png
│  │  │  │  │  │  ├─ lb-r-home_cloud2.png
│  │  │  │  │  │  ├─ lb-r-home_cloud3.png
│  │  │  │  │  │  ├─ lb-r-home_leftflower1.png
│  │  │  │  │  │  ├─ lb-r-home_leftflower2.png
│  │  │  │  │  │  ├─ lb-r-home_out1.png
│  │  │  │  │  │  ├─ lb-r-home_out10.png
│  │  │  │  │  │  ├─ lb-r-home_out11.png
│  │  │  │  │  │  ├─ lb-r-home_out12.png
│  │  │  │  │  │  ├─ lb-r-home_out13.png
│  │  │  │  │  │  ├─ lb-r-home_out14.png
│  │  │  │  │  │  ├─ lb-r-home_out15.png
│  │  │  │  │  │  ├─ lb-r-home_out16.png
│  │  │  │  │  │  ├─ lb-r-home_out17.png
│  │  │  │  │  │  ├─ lb-r-home_out2.png
│  │  │  │  │  │  ├─ lb-r-home_out3.png
│  │  │  │  │  │  ├─ lb-r-home_out4.png
│  │  │  │  │  │  ├─ lb-r-home_out5.png
│  │  │  │  │  │  ├─ lb-r-home_out6.png
│  │  │  │  │  │  ├─ lb-r-home_out7.png
│  │  │  │  │  │  ├─ lb-r-home_out8.png
│  │  │  │  │  │  ├─ lb-r-home_out9.png
│  │  │  │  │  │  ├─ lb-r-home_rightflower1.png
│  │  │  │  │  │  └─ lb-r-home_rightflower2.png
│  │  │  │  │  ├─ hud
│  │  │  │  │  │  ├─ diamond_overlay.png
│  │  │  │  │  │  ├─ energy_progress.png
│  │  │  │  │  │  ├─ object_button.png
│  │  │  │  │  │  ├─ object_talk_chicken.png
│  │  │  │  │  │  ├─ object_talk_mary.png
│  │  │  │  │  │  ├─ oxy_progress.png
│  │  │  │  │  │  ├─ p_object_off.png
│  │  │  │  │  │  ├─ p_object_on.png
│  │  │  │  │  │  ├─ r-energy_bg_1.png
│  │  │  │  │  │  ├─ r-energy_bg_1a.png
│  │  │  │  │  │  ├─ r-energy_bg_1b.png
│  │  │  │  │  │  ├─ r-energy_bg_1c.png
│  │  │  │  │  │  ├─ r-energy_bg_1d.png
│  │  │  │  │  │  ├─ r-energy_bg_1e.png
│  │  │  │  │  │  ├─ r-energy_bg_1f.png
│  │  │  │  │  │  ├─ r-energy_bg_1g.png
│  │  │  │  │  │  ├─ r-energy_bg_1h.png
│  │  │  │  │  │  ├─ r-energy_bg_2.png
│  │  │  │  │  │  ├─ r-energy_bg_2a.png
│  │  │  │  │  │  ├─ r-energy_bg_2b.png
│  │  │  │  │  │  ├─ r-energy_bg_2c.png
│  │  │  │  │  │  ├─ r-energy_bg_2d.png
│  │  │  │  │  │  ├─ r-energy_bg_2e.png
│  │  │  │  │  │  ├─ r-energy_bg_2f.png
│  │  │  │  │  │  ├─ r-energy_bg_3.png
│  │  │  │  │  │  ├─ r-energy_bg_3a.png
│  │  │  │  │  │  ├─ r-energy_bg_3b.png
│  │  │  │  │  │  ├─ r-energy_bg_3c.png
│  │  │  │  │  │  ├─ r-energy_bg_3d.png
│  │  │  │  │  │  ├─ r-energy_bg_4.png
│  │  │  │  │  │  ├─ r-energy_bg_5.png
│  │  │  │  │  │  ├─ r-energy_logo.png
│  │  │  │  │  │  ├─ r-hud_topbutton.png
│  │  │  │  │  │  ├─ r-hud_topbutton1.png
│  │  │  │  │  │  ├─ r-oxy_bg_1.png
│  │  │  │  │  │  ├─ r-oxy_bg_1a.png
│  │  │  │  │  │  ├─ r-oxy_bg_1b.png
│  │  │  │  │  │  ├─ r-oxy_bg_1c.png
│  │  │  │  │  │  ├─ r-oxy_bg_1d.png
│  │  │  │  │  │  ├─ r-oxy_bg_2.png
│  │  │  │  │  │  ├─ r-oxy_bg_2a.png
│  │  │  │  │  │  ├─ r-oxy_bg_2b.png
│  │  │  │  │  │  ├─ r-oxy_bg_2c.png
│  │  │  │  │  │  ├─ r-oxy_bg_2d.png
│  │  │  │  │  │  ├─ r-oxy_bg_2e.png
│  │  │  │  │  │  ├─ r-oxy_bg_2f.png
│  │  │  │  │  │  ├─ r-oxy_bg_2g.png
│  │  │  │  │  │  ├─ r-oxy_bg_3.png
│  │  │  │  │  │  ├─ r-oxy_bg_3a.png
│  │  │  │  │  │  ├─ r-oxy_bg_3b.png
│  │  │  │  │  │  ├─ r-oxy_bg_3c.png
│  │  │  │  │  │  ├─ r-oxy_bg_3d.png
│  │  │  │  │  │  ├─ r-oxy_bg_3e.png
│  │  │  │  │  │  ├─ r-oxy_bg_3f.png
│  │  │  │  │  │  ├─ r-oxy_bg_4.png
│  │  │  │  │  │  ├─ r-oxy_bg_5.png
│  │  │  │  │  │  ├─ r-oxy_logo.png
│  │  │  │  │  │  ├─ sym_diamond.png
│  │  │  │  │  │  └─ sym_money.png
│  │  │  │  │  ├─ hud_energy.png
│  │  │  │  │  ├─ hud_o2.png
│  │  │  │  │  ├─ item
│  │  │  │  │  │  ├─ item_altimeter.png
│  │  │  │  │  │  ├─ item_bag.png
│  │  │  │  │  │  ├─ item_blockgroup.png
│  │  │  │  │  │  ├─ item_c4.png
│  │  │  │  │  │  ├─ item_chest.png
│  │  │  │  │  │  ├─ item_cole.png
│  │  │  │  │  │  ├─ item_diamond.png
│  │  │  │  │  │  ├─ item_drill.png
│  │  │  │  │  │  ├─ item_dynamite0.png
│  │  │  │  │  │  ├─ item_dynamite1.png
│  │  │  │  │  │  ├─ item_energydrink.png
│  │  │  │  │  │  ├─ item_gold.png
│  │  │  │  │  │  ├─ item_goldenpick.png
│  │  │  │  │  │  ├─ item_jetpack.png
│  │  │  │  │  │  ├─ item_lifta.png
│  │  │  │  │  │  ├─ item_liftb.png
│  │  │  │  │  │  ├─ item_pick.png
│  │  │  │  │  │  ├─ item_sabber.png
│  │  │  │  │  │  ├─ item_salt.png
│  │  │  │  │  │  ├─ item_shoe.png
│  │  │  │  │  │  ├─ item_silver.png
│  │  │  │  │  │  ├─ item_sleepingbag.png
│  │  │  │  │  │  ├─ item_spade.png
│  │  │  │  │  │  ├─ item_teleporter.png
│  │  │  │  │  │  ├─ item_yorby.png
│  │  │  │  │  │  ├─ lamp_small.png
│  │  │  │  │  │  ├─ r-overlay_health10.png
│  │  │  │  │  │  ├─ r-overlay_health2.png
│  │  │  │  │  │  ├─ r-overlay_health3.png
│  │  │  │  │  │  ├─ r-overlay_health4.png
│  │  │  │  │  │  ├─ r-overlay_health5.png
│  │  │  │  │  │  ├─ r-overlay_health6.png
│  │  │  │  │  │  ├─ r-overlay_health7.png
│  │  │  │  │  │  ├─ r-overlay_health8.png
│  │  │  │  │  │  ├─ r-overlay_health9.png
│  │  │  │  │  │  ├─ r-overlay_locked.png
│  │  │  │  │  │  ├─ r-overlay_repair.png
│  │  │  │  │  │  ├─ r-overlay_sold.png
│  │  │  │  │  │  ├─ r-overlay_upg2.png
│  │  │  │  │  │  ├─ r-overlay_upg3.png
│  │  │  │  │  │  ├─ r-overlay_upg4.png
│  │  │  │  │  │  ├─ r-overlay_upg5.png
│  │  │  │  │  │  ├─ r-overlay_upg6.png
│  │  │  │  │  │  ├─ r-overlay_upg7.png
│  │  │  │  │  │  ├─ r-overlay_upg8.png
│  │  │  │  │  │  └─ r-overlay_upg9.png
│  │  │  │  │  ├─ lb-px-r-hecke.png
│  │  │  │  │  ├─ lb-r-air.png
│  │  │  │  │  ├─ lb-r-air2.png
│  │  │  │  │  ├─ lb-r-air2_blink0.png
│  │  │  │  │  ├─ lb-r-air2_blink1.png
│  │  │  │  │  ├─ lb-r-air2_front.png
│  │  │  │  │  ├─ lb-r-air_blink0.png
│  │  │  │  │  ├─ lb-r-air_blink1.png
│  │  │  │  │  ├─ lb-r-air_front.png
│  │  │  │  │  ├─ lb-r-automat.png
│  │  │  │  │  ├─ lb-r-automat_1.png
│  │  │  │  │  ├─ lb-r-automat_2.png
│  │  │  │  │  ├─ lb-r-automat_3.png
│  │  │  │  │  ├─ lb-r-automat_4.png
│  │  │  │  │  ├─ lb-r-automat_5.png
│  │  │  │  │  ├─ lb-r-automat_6.png
│  │  │  │  │  ├─ lb-r-automat_game1.png
│  │  │  │  │  ├─ lb-r-automat_game2.png
│  │  │  │  │  ├─ lb-r-automat_game3.png
│  │  │  │  │  ├─ lb-r-automat_game4.png
│  │  │  │  │  ├─ lb-r-automat_game5.png
│  │  │  │  │  ├─ lb-r-automat_game6.png
│  │  │  │  │  ├─ lb-r-fire1.png
│  │  │  │  │  ├─ lb-r-fire2.png
│  │  │  │  │  ├─ lb-r-garage.png
│  │  │  │  │  ├─ lb-r-garage_cloud1.png
│  │  │  │  │  ├─ lb-r-garage_cloud2.png
│  │  │  │  │  ├─ lb-r-garage_cloud3.png
│  │  │  │  │  ├─ lb-r-garage_name1.png
│  │  │  │  │  ├─ lb-r-garage_name2.png
│  │  │  │  │  ├─ lb-r-garage_name3.png
│  │  │  │  │  ├─ lb-r-garage_name4.png
│  │  │  │  │  ├─ lb-r-garage_work1.png
│  │  │  │  │  ├─ lb-r-garage_work2.png
│  │  │  │  │  ├─ lb-r-garage_work3.png
│  │  │  │  │  ├─ lb-r-generator.png
│  │  │  │  │  ├─ lb-r-generator2.png
│  │  │  │  │  ├─ lb-r-generator3.png
│  │  │  │  │  ├─ lb-r-generator4.png
│  │  │  │  │  ├─ lb-r-generator5.png
│  │  │  │  │  ├─ lb-r-generator_status1.png
│  │  │  │  │  ├─ lb-r-generator_status2.png
│  │  │  │  │  ├─ lb-r-generator_status3.png
│  │  │  │  │  ├─ lb-r-generator_status4.png
│  │  │  │  │  ├─ lb-r-generator_status5.png
│  │  │  │  │  ├─ lb-r-generator_status6.png
│  │  │  │  │  ├─ lb-r-mega_lift.png
│  │  │  │  │  ├─ lb-r-mega_lift_ani0.png
│  │  │  │  │  ├─ lb-r-mega_lift_ani1.png
│  │  │  │  │  ├─ lb-r-mine.png
│  │  │  │  │  ├─ lb-r-mine_box_1.png
│  │  │  │  │  ├─ lb-r-mine_box_2.png
│  │  │  │  │  ├─ lb-r-mine_cloud1.png
│  │  │  │  │  ├─ lb-r-mine_cloud2.png
│  │  │  │  │  ├─ lb-r-mine_cloud3.png
│  │  │  │  │  ├─ lb-r-mine_entry.png
│  │  │  │  │  ├─ lb-r-mine_fence.png
│  │  │  │  │  ├─ lb-r-mine_name0.png
│  │  │  │  │  ├─ lb-r-mine_name1.png
│  │  │  │  │  ├─ lb-r-mine_name2.png
│  │  │  │  │  ├─ lb-r-mine_name3.png
│  │  │  │  │  ├─ lb-r-mine_name4.png
│  │  │  │  │  ├─ lb-r-palm.png
│  │  │  │  │  ├─ lb-r-rocket_building.png
│  │  │  │  │  ├─ lb-r-shop.png
│  │  │  │  │  ├─ lb-r-shop_flower.png
│  │  │  │  │  ├─ lb-r-shop_name.png
│  │  │  │  │  ├─ lb-r-statue_golem.png
│  │  │  │  │  ├─ lb-r-statue_golem1.png
│  │  │  │  │  ├─ lb-r-statue_golem2.png
│  │  │  │  │  ├─ lb-r-stone_border_left.png
│  │  │  │  │  ├─ lb-r-stone_border_right.png
│  │  │  │  │  ├─ lb-r-tree2.png
│  │  │  │  │  ├─ lt-py-slider_off.png
│  │  │  │  │  ├─ lt-py-slider_on.png
│  │  │  │  │  ├─ mine_wheel.png
│  │  │  │  │  ├─ npc
│  │  │  │  │  │  ├─ bird_one_1.png
│  │  │  │  │  │  ├─ bird_one_2.png
│  │  │  │  │  │  ├─ bird_two_1.png
│  │  │  │  │  │  ├─ bird_two_2.png
│  │  │  │  │  │  ├─ lkw_wheel.png
│  │  │  │  │  │  ├─ r-cb-chick_pick_b.png
│  │  │  │  │  │  ├─ r-cb-chick_stand_a.png
│  │  │  │  │  │  ├─ r-cb-chick_stand_b.png
│  │  │  │  │  │  ├─ r-cb-chick_walk_b.png
│  │  │  │  │  │  ├─ r-cb-hen_pick_b.png
│  │  │  │  │  │  ├─ r-cb-hen_stand_a.png
│  │  │  │  │  │  ├─ r-cb-hen_stand_b.png
│  │  │  │  │  │  ├─ r-cb-hen_walk_b.png
│  │  │  │  │  │  ├─ r-cb-lkw2_1.png
│  │  │  │  │  │  ├─ r-cb-lkw2_2.png
│  │  │  │  │  │  ├─ r-cb-lkw_1.png
│  │  │  │  │  │  └─ r-cb-lkw_2.png
│  │  │  │  │  ├─ orderbuilding
│  │  │  │  │  │  ├─ lb-r-mary_idle1.png
│  │  │  │  │  │  ├─ lb-r-mary_idle2.png
│  │  │  │  │  │  ├─ lb-r-mary_idle3.png
│  │  │  │  │  │  ├─ lb-r-mary_speak1.png
│  │  │  │  │  │  ├─ lb-r-mary_speak2.png
│  │  │  │  │  │  ├─ lb-r-mary_stand.png
│  │  │  │  │  │  ├─ lb-r-mary_stand2.png
│  │  │  │  │  │  ├─ lb-r-orders.png
│  │  │  │  │  │  ├─ lb-r-orders_board1.png
│  │  │  │  │  │  ├─ lb-r-orders_board2.png
│  │  │  │  │  │  ├─ lb-r-orders_board3.png
│  │  │  │  │  │  └─ lb-r-orders_name.png
│  │  │  │  │  ├─ order_btn1.png
│  │  │  │  │  ├─ order_btn2.png
│  │  │  │  │  ├─ order_btn3.png
│  │  │  │  │  ├─ order_btn4.png
│  │  │  │  │  ├─ order_btn5.png
│  │  │  │  │  ├─ order_btn6.png
│  │  │  │  │  ├─ order_payout.png
│  │  │  │  │  ├─ order_txtfield.png
│  │  │  │  │  ├─ particle
│  │  │  │  │  │  ├─ notice_here.png
│  │  │  │  │  │  ├─ notice_ready.png
│  │  │  │  │  │  ├─ p_earth.png
│  │  │  │  │  │  ├─ p_money.png
│  │  │  │  │  │  ├─ p_smoke.png
│  │  │  │  │  │  ├─ p_stone.png
│  │  │  │  │  │  ├─ r-p_exp0.png
│  │  │  │  │  │  ├─ r-p_exp1.png
│  │  │  │  │  │  ├─ r-p_exp2.png
│  │  │  │  │  │  ├─ r-p_exp3.png
│  │  │  │  │  │  ├─ r-p_exp4.png
│  │  │  │  │  │  ├─ r-p_exp5.png
│  │  │  │  │  │  ├─ r-p_exp6.png
│  │  │  │  │  │  ├─ r-p_exp7.png
│  │  │  │  │  │  ├─ r-p_exp8.png
│  │  │  │  │  │  ├─ r-p_exp9.png
│  │  │  │  │  │  └─ r-p_ring.png
│  │  │  │  │  ├─ placeholder.png
│  │  │  │  │  ├─ plants
│  │  │  │  │  │  ├─ cb-r-grape_f1.png
│  │  │  │  │  │  ├─ cb-r-grape_f2.png
│  │  │  │  │  │  ├─ cb-r-grape_f3.png
│  │  │  │  │  │  ├─ cb-r-grape_f4.png
│  │  │  │  │  │  ├─ cb-r-grape_f5.png
│  │  │  │  │  │  ├─ lb-fl_carrote_0.png
│  │  │  │  │  │  ├─ lb-fl_carrote_1.png
│  │  │  │  │  │  ├─ lb-fl_carrote_2.png
│  │  │  │  │  │  ├─ lb-fl_carrote_3.png
│  │  │  │  │  │  ├─ lb-r-fl_tomato_0.png
│  │  │  │  │  │  ├─ lb-r-fl_tomato_1.png
│  │  │  │  │  │  ├─ lb-r-fl_tomato_2.png
│  │  │  │  │  │  ├─ lb-r-fl_tomato_3.png
│  │  │  │  │  │  ├─ lb-r-fl_tomato_4.png
│  │  │  │  │  │  ├─ lb-r-fl_tomato_5.png
│  │  │  │  │  │  ├─ lb-r-fl_tomato_6.png
│  │  │  │  │  │  ├─ lb-r-fl_tomato_7.png
│  │  │  │  │  │  ├─ lb-r-grape_0.png
│  │  │  │  │  │  ├─ lb-r-grape_1.png
│  │  │  │  │  │  ├─ lb-r-grape_10.png
│  │  │  │  │  │  ├─ lb-r-grape_2.png
│  │  │  │  │  │  ├─ lb-r-grape_3.png
│  │  │  │  │  │  ├─ lb-r-grape_4.png
│  │  │  │  │  │  ├─ lb-r-grape_5.png
│  │  │  │  │  │  ├─ lb-r-grape_6.png
│  │  │  │  │  │  ├─ lb-r-grape_7.png
│  │  │  │  │  │  ├─ lb-r-grape_8.png
│  │  │  │  │  │  ├─ lb-r-grape_9.png
│  │  │  │  │  │  └─ lb-r-landscape_tree.png
│  │  │  │  │  ├─ progress_back.png
│  │  │  │  │  ├─ progress_front.png
│  │  │  │  │  ├─ pxy-buildconstruction.png
│  │  │  │  │  ├─ shop
│  │  │  │  │  │  ├─ product_carrote_seed.png
│  │  │  │  │  │  ├─ product_grape_seed.png
│  │  │  │  │  │  ├─ product_tomato_seed.png
│  │  │  │  │  │  ├─ r-shop_health.png
│  │  │  │  │  │  ├─ shop_active.png
│  │  │  │  │  │  ├─ shop_air.png
│  │  │  │  │  │  ├─ shop_air2.png
│  │  │  │  │  │  ├─ shop_bagslot.png
│  │  │  │  │  │  ├─ shop_bagweight.png
│  │  │  │  │  │  ├─ shop_block1.png
│  │  │  │  │  │  ├─ shop_blue.png
│  │  │  │  │  │  ├─ shop_bridge.png
│  │  │  │  │  │  ├─ shop_cloud1.png
│  │  │  │  │  │  ├─ shop_cloud2.png
│  │  │  │  │  │  ├─ shop_cloud3.png
│  │  │  │  │  │  ├─ shop_deletebuilding.png
│  │  │  │  │  │  ├─ shop_description.png
│  │  │  │  │  │  ├─ shop_diamond1.png
│  │  │  │  │  │  ├─ shop_diamond2.png
│  │  │  │  │  │  ├─ shop_diamond3.png
│  │  │  │  │  │  ├─ shop_diamond4.png
│  │  │  │  │  │  ├─ shop_diamond5.png
│  │  │  │  │  │  ├─ shop_energydrink.png
│  │  │  │  │  │  ├─ shop_garage.png
│  │  │  │  │  │  ├─ shop_generator.png
│  │  │  │  │  │  ├─ shop_goldenpick.png
│  │  │  │  │  │  ├─ shop_golem.png
│  │  │  │  │  │  ├─ shop_green.png
│  │  │  │  │  │  ├─ shop_grey.png
│  │  │  │  │  │  ├─ shop_hecke.png
│  │  │  │  │  │  ├─ shop_jetpack.png
│  │  │  │  │  │  ├─ shop_ladder1.png
│  │  │  │  │  │  ├─ shop_ladder6.png
│  │  │  │  │  │  ├─ shop_megalift.png
│  │  │  │  │  │  ├─ shop_megalift2.png
│  │  │  │  │  │  ├─ shop_megalift3.png
│  │  │  │  │  │  ├─ shop_money1.png
│  │  │  │  │  │  ├─ shop_money2.png
│  │  │  │  │  │  ├─ shop_money3.png
│  │  │  │  │  │  ├─ shop_movebuilding.png
│  │  │  │  │  │  ├─ shop_noads.png
│  │  │  │  │  │  ├─ shop_palm.png
│  │  │  │  │  │  ├─ shop_red.png
│  │  │  │  │  │  ├─ shop_rocket.png
│  │  │  │  │  │  ├─ shop_shoe.png
│  │  │  │  │  │  ├─ shop_sign1.png
│  │  │  │  │  │  ├─ shop_sign2.png
│  │  │  │  │  │  ├─ shop_sign3.png
│  │  │  │  │  │  ├─ shop_sign4.png
│  │  │  │  │  │  ├─ shop_sign5.png
│  │  │  │  │  │  ├─ shop_specialoffer.png
│  │  │  │  │  │  ├─ shop_tilelamp.png
│  │  │  │  │  │  ├─ shop_tilelamp2.png
│  │  │  │  │  │  ├─ shop_tree.png
│  │  │  │  │  │  ├─ shop_tree2.png
│  │  │  │  │  │  ├─ shop_yellow.png
│  │  │  │  │  │  ├─ symbol_freehand.png
│  │  │  │  │  │  └─ symbol_yes.png
│  │  │  │  │  ├─ shop_arrow0.png
│  │  │  │  │  ├─ shop_arrow1.png
│  │  │  │  │  ├─ spider
│  │  │  │  │  │  ├─ r-spider1a.png
│  │  │  │  │  │  ├─ r-spider1b.png
│  │  │  │  │  │  ├─ r-spider1c.png
│  │  │  │  │  │  ├─ r-spider2a.png
│  │  │  │  │  │  ├─ r-spider2b.png
│  │  │  │  │  │  └─ r-spider2c.png
│  │  │  │  │  ├─ sym_crafted0.png
│  │  │  │  │  ├─ sym_crafted1.png
│  │  │  │  │  ├─ sym_credit.png
│  │  │  │  │  ├─ sym_dead.png
│  │  │  │  │  ├─ sym_electricity.png
│  │  │  │  │  ├─ sym_exclamation.png
│  │  │  │  │  ├─ sym_stat.png
│  │  │  │  │  ├─ sym_web.png
│  │  │  │  │  ├─ table
│  │  │  │  │  │  ├─ lt-r-px-tableborder2_40.png
│  │  │  │  │  │  ├─ lt-r-px-tableborder_40.png
│  │  │  │  │  │  └─ trenner_40.png
│  │  │  │  │  ├─ tiles
│  │  │  │  │  │  ├─ pxy-block_2.png
│  │  │  │  │  │  ├─ pxy-block_2a.png
│  │  │  │  │  │  ├─ pxy-block_2b.png
│  │  │  │  │  │  ├─ pxy-block_2c.png
│  │  │  │  │  │  ├─ pxy-block_2d.png
│  │  │  │  │  │  ├─ pxy-block_2e.png
│  │  │  │  │  │  ├─ pxy-block_2f.png
│  │  │  │  │  │  ├─ pxy-block_2g.png
│  │  │  │  │  │  ├─ pxy-block_2h.png
│  │  │  │  │  │  ├─ pxy-block_3.png
│  │  │  │  │  │  ├─ pxy-border.png
│  │  │  │  │  │  ├─ pxy-dungeon.png
│  │  │  │  │  │  ├─ pxy-earth_0.png
│  │  │  │  │  │  ├─ pxy-earth_1.png
│  │  │  │  │  │  ├─ pxy-earth_2.png
│  │  │  │  │  │  ├─ pxy-earth_3.png
│  │  │  │  │  │  ├─ pxy-earth_4.png
│  │  │  │  │  │  ├─ pxy-earth_5.png
│  │  │  │  │  │  ├─ pxy-earth_6.png
│  │  │  │  │  │  ├─ pxy-earth_7.png
│  │  │  │  │  │  ├─ pxy-earth_8.png
│  │  │  │  │  │  ├─ pxy-earth_9.png
│  │  │  │  │  │  ├─ pxy-earth_crafted.png
│  │  │  │  │  │  ├─ pxy-lava.png
│  │  │  │  │  │  ├─ pxy-lava_2.png
│  │  │  │  │  │  ├─ pxy-lava_2a.png
│  │  │  │  │  │  ├─ pxy-new_block.png
│  │  │  │  │  │  ├─ pxy-shadow.png
│  │  │  │  │  │  ├─ pxy-spidernest1.png
│  │  │  │  │  │  ├─ pxy-spidernest2.png
│  │  │  │  │  │  ├─ pxy-spidernet0.png
│  │  │  │  │  │  ├─ pxy-surface_1.png
│  │  │  │  │  │  ├─ pxy-surface_2.png
│  │  │  │  │  │  ├─ pxy-surface_3.png
│  │  │  │  │  │  ├─ pxy-tile_lamp2_0.png
│  │  │  │  │  │  ├─ pxy-tile_lamp2_1.png
│  │  │  │  │  │  ├─ pxy-tile_lamp2_2.png
│  │  │  │  │  │  ├─ pxy-tile_lamp_0.png
│  │  │  │  │  │  ├─ pxy-tile_lamp_1.png
│  │  │  │  │  │  ├─ pxy-tile_lamp_2.png
│  │  │  │  │  │  ├─ pxy-tile_lift_a0.png
│  │  │  │  │  │  ├─ pxy-tile_lift_b0.png
│  │  │  │  │  │  ├─ pxy-tile_megalift_0.png
│  │  │  │  │  │  ├─ pxy-tile_megalift_1.png
│  │  │  │  │  │  ├─ pxy-tile_megalift_off.png
│  │  │  │  │  │  ├─ pxy-tile_no.png
│  │  │  │  │  │  ├─ pxy-tile_yes.png
│  │  │  │  │  │  ├─ pxy-wall_0.png
│  │  │  │  │  │  ├─ pxy-wall_1.png
│  │  │  │  │  │  ├─ pxy-wall_2.png
│  │  │  │  │  │  ├─ pxy-wall_3.png
│  │  │  │  │  │  ├─ pxy-wall_4.png
│  │  │  │  │  │  ├─ pxy-wall_5.png
│  │  │  │  │  │  ├─ py-tile_lift_a1.png
│  │  │  │  │  │  ├─ py-tile_lift_b1.png
│  │  │  │  │  │  ├─ r-artefact_bone1.png
│  │  │  │  │  │  ├─ r-artefact_bone2.png
│  │  │  │  │  │  ├─ r-artefact_g1.png
│  │  │  │  │  │  ├─ r-artefact_g2.png
│  │  │  │  │  │  ├─ r-artefact_g3.png
│  │  │  │  │  │  ├─ r-artefact_g4.png
│  │  │  │  │  │  ├─ r-artefact_ring.png
│  │  │  │  │  │  ├─ r-cole.png
│  │  │  │  │  │  ├─ r-diamond_blue.png
│  │  │  │  │  │  ├─ r-diamond_green.png
│  │  │  │  │  │  ├─ r-diamond_pink.png
│  │  │  │  │  │  ├─ r-diamond_red.png
│  │  │  │  │  │  ├─ r-diamond_small_blue.png
│  │  │  │  │  │  ├─ r-diamond_small_green.png
│  │  │  │  │  │  ├─ r-diamond_small_pink.png
│  │  │  │  │  │  ├─ r-emerald_blue.png
│  │  │  │  │  │  ├─ r-emerald_red.png
│  │  │  │  │  │  ├─ r-emerald_yellow.png
│  │  │  │  │  │  ├─ r-gold.png
│  │  │  │  │  │  ├─ r-iron.png
│  │  │  │  │  │  ├─ r-landscape_deco0.png
│  │  │  │  │  │  ├─ r-landscape_deco1a.png
│  │  │  │  │  │  ├─ r-landscape_deco1b.png
│  │  │  │  │  │  ├─ r-landscape_deco1c.png
│  │  │  │  │  │  ├─ r-landscape_deco2a.png
│  │  │  │  │  │  ├─ r-landscape_deco2b.png
│  │  │  │  │  │  ├─ r-landscape_deco2c.png
│  │  │  │  │  │  ├─ r-landscape_deco3a.png
│  │  │  │  │  │  ├─ r-landscape_deco3b.png
│  │  │  │  │  │  ├─ r-landscape_deco3c.png
│  │  │  │  │  │  ├─ r-landscape_deco4a.png
│  │  │  │  │  │  ├─ r-landscape_deco4b.png
│  │  │  │  │  │  ├─ r-landscape_deco4c.png
│  │  │  │  │  │  ├─ r-lazurite.png
│  │  │  │  │  │  ├─ r-monster0.png
│  │  │  │  │  │  ├─ r-monster1.png
│  │  │  │  │  │  ├─ r-monster2.png
│  │  │  │  │  │  ├─ r-obj_cole.png
│  │  │  │  │  │  ├─ r-obj_diamond_blue.png
│  │  │  │  │  │  ├─ r-obj_diamond_green.png
│  │  │  │  │  │  ├─ r-obj_diamond_pink.png
│  │  │  │  │  │  ├─ r-obj_diamond_red.png
│  │  │  │  │  │  ├─ r-obj_diamond_small_blue.png
│  │  │  │  │  │  ├─ r-obj_diamond_small_green.png
│  │  │  │  │  │  ├─ r-obj_diamond_small_pink.png
│  │  │  │  │  │  ├─ r-obj_emerald_blue.png
│  │  │  │  │  │  ├─ r-obj_emerald_red.png
│  │  │  │  │  │  ├─ r-obj_emerald_yellow.png
│  │  │  │  │  │  ├─ r-obj_gold.png
│  │  │  │  │  │  ├─ r-obj_iron.png
│  │  │  │  │  │  ├─ r-obj_lazurite.png
│  │  │  │  │  │  ├─ r-obj_patrickium.png
│  │  │  │  │  │  ├─ r-obj_platin.png
│  │  │  │  │  │  ├─ r-obj_ruby.png
│  │  │  │  │  │  ├─ r-obj_salt.png
│  │  │  │  │  │  ├─ r-obj_sapphire.png
│  │  │  │  │  │  ├─ r-obj_silver.png
│  │  │  │  │  │  ├─ r-obj_uranium.png
│  │  │  │  │  │  ├─ r-obj_yorby.png
│  │  │  │  │  │  ├─ r-patrickium.png
│  │  │  │  │  │  ├─ r-platin.png
│  │  │  │  │  │  ├─ r-px-tile_bridge.png
│  │  │  │  │  │  ├─ r-px-tile_gras1.png
│  │  │  │  │  │  ├─ r-px-tile_gras2.png
│  │  │  │  │  │  ├─ r-px-tile_gras3.png
│  │  │  │  │  │  ├─ r-pxy-tile_ladderbridge.png
│  │  │  │  │  │  ├─ r-py-object_ladder.png
│  │  │  │  │  │  ├─ r-ruby.png
│  │  │  │  │  │  ├─ r-salt.png
│  │  │  │  │  │  ├─ r-sapphire.png
│  │  │  │  │  │  ├─ r-silver.png
│  │  │  │  │  │  ├─ r-tile_c4_0.png
│  │  │  │  │  │  ├─ r-tile_c4_1.png
│  │  │  │  │  │  ├─ r-tile_damage1.png
│  │  │  │  │  │  ├─ r-tile_damage2.png
│  │  │  │  │  │  ├─ r-tile_damage3.png
│  │  │  │  │  │  ├─ r-tile_damage4.png
│  │  │  │  │  │  ├─ r-tile_deco_0.png
│  │  │  │  │  │  ├─ r-tile_deco_1.png
│  │  │  │  │  │  ├─ r-tile_deco_2.png
│  │  │  │  │  │  ├─ r-tile_dynamite1_0.png
│  │  │  │  │  │  ├─ r-tile_dynamite1_1.png
│  │  │  │  │  │  ├─ r-tile_dynamite2_0.png
│  │  │  │  │  │  ├─ r-tile_dynamite2_1.png
│  │  │  │  │  │  ├─ r-tile_sign_0.png
│  │  │  │  │  │  ├─ r-tile_sign_1.png
│  │  │  │  │  │  ├─ r-tile_sign_2.png
│  │  │  │  │  │  ├─ r-tile_sign_3.png
│  │  │  │  │  │  ├─ r-tile_sign_4.png
│  │  │  │  │  │  ├─ r-uranium.png
│  │  │  │  │  │  ├─ r-yorbinium.png
│  │  │  │  │  │  ├─ rock.png
│  │  │  │  │  │  ├─ spidernet1.png
│  │  │  │  │  │  ├─ spidernet2.png
│  │  │  │  │  │  ├─ spidernet3.png
│  │  │  │  │  │  ├─ spidernet4.png
│  │  │  │  │  │  └─ stone.png
│  │  │  │  │  └─ txtbox
│  │  │  │  │     ├─ chicken0.png
│  │  │  │  │     ├─ chicken1.png
│  │  │  │  │     ├─ dwarf0.png
│  │  │  │  │     ├─ dwarf1.png
│  │  │  │  │     ├─ mary0.png
│  │  │  │  │     ├─ mary1.png
│  │  │  │  │     ├─ miner0.png
│  │  │  │  │     ├─ miner1.png
│  │  │  │  │     ├─ rm-textbox.png
│  │  │  │  │     └─ textbox_btn.png
│  │  │  │  └─ media-atlas
│  │  │  │     ├─ gameatlas_0.png
│  │  │  │     ├─ gameatlas_1.png
│  │  │  │     ├─ gameatlas_2.png
│  │  │  │     ├─ gameatlas_3.png
│  │  │  │     ├─ gameatlas_4.png
│  │  │  │     ├─ gameatlas_5.png
│  │  │  │     └─ gameatlas_6.png
│  │  │  ├─ tilemap.tmx
│  │  │  ├─ tileset.tps
│  │  │  ├─ tileset.tsx
│  │  │  ├─ treasurehunt.tmx
│  │  │  └─ treasurehunt.tps
│  │  ├─ tilemap.json
│  │  ├─ tileset.json
│  │  └─ tileset.png
│  ├─ index.js
│  ├─ main.js
│  ├─ messagelog.js
│  ├─ multiplayer
│  │  ├─ match.js
│  │  ├─ message.js
│  │  └─ session.js
│  ├─ multiplayer.js
│  └─ player.js
├─ webpack
│  ├─ base.js
│  └─ prod.js
└─ yarn.lock

```