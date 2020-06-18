<div class="input-group">
	<input class="form-control py-2 border-right-0 border" type="text" id="searchBar" onkeyup="filterShadows()" placeholder="Search for shadows by name, description, personality etc.." title="Type in a shadow">
	<span class="input-group-append">
		<div class="input-group-text bg-transparent"><i class="fa fa-search"></i></div>
	</span>
</div>

<script>
function filterShadows() {
   var input, filter, headers, tables, tableRowCount, tr;
   input = document.getElementById("searchBar");
   filter = input.value.toUpperCase();
   headers = document.getElementsByTagName("h5");
   tables = document.getElementsByTagName("table");
   tableRowCount = [];

   for (i = 0; i < tables.length; i++) {
      tableRowCount.push(tables[i].rows.length);
   }
   
   for (i = 0; i < tables.length; i++) {
      tr = tables[i].getElementsByTagName("tr");
      var hiddenCount = 0;

      for (j = 0; j < tr.length; j++) {
         td = tr[j].getElementsByTagName("td")[0];
         if (td) {
            var nameCol = tr[j].getElementsByTagName("td")[0].textContent.toUpperCase();
            var desCol = tr[j].getElementsByTagName("td")[1].textContent.toUpperCase();
            var arcCol = tr[j].getElementsByTagName("td")[2].textContent.toUpperCase();
            var perCol = tr[j].getElementsByTagName("td")[3].textContent.toUpperCase();
            if (nameCol.indexOf(filter) > -1 || desCol.indexOf(filter) > -1 || arcCol.indexOf(filter) > -1 || perCol.indexOf(filter) > -1) {
               tr[j].style.display = "";
            } else {
               tr[j].style.display = "none";
               hiddenCount = hiddenCount + 1;
            }
         }
      }

      if (hiddenCount == tableRowCount[i] - 1) {
         tables[i].style.display = "none";
         headers[i].style.display = "none";
      } else {
         tables[i].style.display = "";
         headers[i].style.display = "";
      }
   }
}
</script>

<br>

##### Kamoshida's Palace

<table>
   <tr>
      <th>Persona</th>
      <th>Shadow</th>
      <th>Arcana</th>
      <th>Personality</th>
      <th>Weakness</th>
   </tr>
   <tr>
      <td>Jack-o'-Lantern</td>
      <td>Crypt-dwelling Pyromaniac</td>
      <td>Magician</td>
      <td>Gloomy</td>
      <td>Ice, Wind</td>
   </tr>
   <tr>
      <td>Pixie</td>
      <td>Beguiling Girl</td>
      <td>Lovers</td>
      <td>Timid</td>
      <td>Gun, Ice, Curse</td>
   </tr>
   <tr>
      <td>Incubus</td>
      <td>Bedside Brute</td>
      <td>Devil</td>
      <td>Timid</td>
      <td>Fire, Bless</td>
   </tr>
   <tr>
      <td>Mandrake</td>
      <td>Gallows Flower</td>
      <td>Death</td>
      <td>Upbeat</td>
      <td>Fire</td>
   </tr>
   <tr>
      <td>Bicorn</td>
      <td>Dirty Two-horned Beast</td>
      <td>Hermit</td>
      <td>Gloomy</td>
      <td>Electric</td>
   </tr>
   <tr>
      <td>Agathion</td>
      <td>Apprentice in a Jug</td>
      <td>Chariot</td>
      <td>Timid</td>
      <td>Wind</td>
   </tr>
   <tr>
      <td>Berith</td>
      <td>Brutal Cavalryman</td>
      <td>Hierophant</td>
      <td>Irritable</td>
      <td>Ice</td>
   </tr>
   <tr>
      <td>Silky</td>
      <td>Troublesome Housemaid</td>
      <td>Priestess</td>
      <td>Gloomy</td>
      <td>Fire, Electric</td>
   </tr>
   <tr>
      <td>Kelpie</td>
      <td>Mad Marsh Horse</td>
      <td>Strength</td>
      <td>Gloomy</td>
      <td>Electric</td>
   </tr>
   <tr>
      <td>Succubus</td>
      <td>Twilight Prostitute</td>
      <td>Moon</td>
      <td>Gloomy</td>
      <td>Wind, Bless</td>
   </tr>
   <tr>
      <td>Eligor</td>
      <td>War-hungry Horseman</td>
      <td>Emperor</td>
      <td>Upbeat</td>
      <td>Electric</td>
   </tr>
   <tr>
      <td>Archangel</td>
      <td>Heavenly Punisher</td>
      <td>Justice</td>
      <td>Irritable</td>
      <td>Electric, Curse</td>
   </tr>
   <tr>
      <td>Cait Sith <span class="badge badge-danger">Royal</span></td>
      <td>Hunting Puss in Boots</td>
      <td>Magician</td>
      <td>Upbeat</td>
      <td>Wind</td>
   </tr>
   <tr>
      <td>Angel</td>
      <td>Zealous Messenger</td>
      <td>Justice</td>
      <td>Upbeat</td>
      <td>Gun, Curse</td>
   </tr>
</table>

##### Madarame's Palace

<table>
   <tr>
      <th>Persona</th>
      <th>Shadow</th>
      <th>Arcana</th>
      <th>Personality</th>
      <th>Weakness</th>
   </tr>
   <tr>
      <td>Mokoi</td>
      <td>Night-Walking Warrior</td>
      <td>Death</td>
      <td>Gloomy</td>
      <td>Wind</td>
   </tr>
   <tr>
      <td>Apsaras</td>
      <td>Waterside Nymph</td>
      <td>Priestess</td>
      <td>Timid</td>
      <td>Fire, Electric</td>
   </tr>
   <tr>
      <td>Hua Po</td>
      <td>Girl of the Hanging Tree</td>
      <td>Hanged Man</td>
      <td>Irritable</td>
      <td>Gun, Ice</td>
   </tr>
   <tr>
      <td>Koropokguru</td>
      <td>Leafy Old Man</td>
      <td>Hermit</td>
      <td>Timid</td>
      <td>Fire</td>
   </tr>
   <tr>
      <td>Onmoraki</td>
      <td>Corpse Bird</td>
      <td>Moon</td>
      <td>Gloomy</td>
      <td>Ice, Bless</td>
   </tr>
   <tr>
      <td>Ippon-Datara</td>
      <td>Embittered Blacksmith</td>
      <td>Hermit</td>
      <td>Timid</td>
      <td>Ice</td>
   </tr>
   <tr>
      <td>Koppa Tengu</td>
      <td>Foolish Monk</td>
      <td>Temperance</td>
      <td>Upbeat</td>
      <td>Ice, Bless</td>
   </tr>
   <tr>
      <td>Nue</td>
      <td>Night Chimera</td>
      <td>Death</td>
      <td>Irritable</td>
      <td>Fire</td>
   </tr>
   <tr>
      <td>Jack Frost</td>
      <td>Mocking Snowman</td>
      <td>Magician</td>
      <td>Timid</td>
      <td>Fire</td>
   </tr>
   <tr>
      <td>Makami</td>
      <td>Hunting Wolf Spirit</td>
      <td>Temperance</td>
      <td>Gloomy</td>
      <td>Electric</td>
   </tr>
   <tr>
      <td>Inugami</td>
      <td>Possessing Dog Ghost</td>
      <td>Hanged Man</td>
      <td>Timid</td>
      <td>Wind</td>
   </tr>
   <tr>
      <td>Shiki-Ouji</td>
      <td>Bringer of Misfortune</td>
      <td>Chariot</td>
      <td>Irritable</td>
      <td>Nuclear</td>
   </tr>
   <tr>
      <td>Shiisaa <span class="badge badge-danger">Royal</span></td>
      <td>Rooftop Lion</td>
      <td>Strength</td>
      <td>Upbeat</td>
      <td>Curse</td>
   </tr>
   <tr>
      <td>Ame-no-Uzume <span class="badge badge-danger">Royal</span></td>
      <td>Captivating Dancer</td>
      <td>Lovers</td>
      <td>Upbeat</td>
      <td>Psychic</td>
   </tr>
</table>

##### Kaneshiro's Palace

<table>
   <tr>
      <th>Persona</th>
      <th>Shadow</th>
      <th>Arcana</th>
      <th>Personality</th>
      <th>Weakness</th>
   </tr>
   <tr>
      <td>Nekomata</td>
      <td>Ascended Feline</td>
      <td>Magician</td>
      <td>Upbeat</td>
      <td>Electric</td>
   </tr>
   <tr>
      <td>High Pixie</td>
      <td>Prankster Leader</td>
      <td>Fool</td>
      <td>Upbeat</td>
      <td>Gun, Nuclear</td>
   </tr>
   <tr>
      <td>Angel</td>
      <td>Zealous Messenger</td>
      <td>Justice</td>
      <td>Upbeat</td>
      <td>Gun, Curse</td>
   </tr>
   <tr>
      <td>Orthrus</td>
      <td>Twin-headed Guardian</td>
      <td>Hanged Man</td>
      <td>Gloomy</td>
      <td>Ice</td>
   </tr>
   <tr>
      <td>Orobas</td>
      <td>Equine Sage</td>
      <td>Hierophant</td>
      <td>?</td>
      <td>Ice</td>
   </tr>
   <tr>
      <td>Oni</td>
      <td>Chivalrous Fiend</td>
      <td>Strength</td>
      <td>Upbeat</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Yaksini</td>
      <td>Human-eating Lady</td>
      <td>Empress</td>
      <td>Irritable</td>
      <td>Nuclear</td>
   </tr>
   <tr>
      <td>Leanan Sidhe</td>
      <td>Jealous Lover</td>
      <td>Lovers</td>
      <td>Timid</td>
      <td>Fire</td>
   </tr>
   <tr>
      <td>Rakshasa</td>
      <td>Battle Fiend</td>
      <td>Strength</td>
      <td>Upbeat</td>
      <td>Wind, Bless</td>
   </tr>
   <tr>
      <td>Take-Minakata</td>
      <td>Defeated Avenger</td>
      <td>Hanged Man</td>
      <td>Irritable</td>
      <td>Psychic</td>
   </tr>
   <tr>
      <td>Kurama Tengu</td>
      <td>Monk of the Valley</td>
      <td>Hermit</td>
      <td>Irritable</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Black Ooze</td>
      <td>Pulsing Mud</td>
      <td>Moon</td>
      <td>Timid</td>
      <td>Electric, Psychic, Bless</td>
   </tr>
   <tr>
      <td>Sui-ki</td>
      <td>Raging Water Demon</td>
      <td>Moon</td>
      <td>Gloomy</td>
      <td>Nuclear</td>
   </tr>
   <tr>
      <td>Fuu-ki</td>
      <td>Tornado Devil</td>
      <td>Star</td>
      <td>Gloomy</td>
      <td>Electric</td>
   </tr>
   <tr>
      <td>Kin-ki</td>
      <td>Samurai Killer</td>
      <td>Chariot</td>
      <td>Irritable</td>
      <td>None</td>
   </tr>
</table>

##### Futaba's Palace

<table>
   <tr>
      <th>Persona</th>
      <th>Shadow</th>
      <th>Arcana</th>
      <th>Personality</th>
      <th>Weakness</th>
   </tr>
   <tr>
      <td>Sandman</td>
      <td>Envoy of Slumber</td>
      <td>Magician</td>
      <td>Upbeat</td>
      <td>Fire, Electric</td>
   </tr>
   <tr>
      <td>Anzu</td>
      <td>Thief of Tablets</td>
      <td>Hierophant</td>
      <td>Timid</td>
      <td>Gun, Nuclear</td>
   </tr>
   <tr>
      <td>Naga</td>
      <td>Cavern Snakeman</td>
      <td>Hermit</td>
      <td>Gloomy</td>
      <td>Wind</td>
   </tr>
   <tr>
      <td>Lamia</td>
      <td>Slithering Snakewoman</td>
      <td>Empress</td>
      <td>Gloomy</td>
      <td>Ice, Nuclear</td>
   </tr>
   <tr>
      <td>Thoth</td>
      <td>Chanting Baboon</td>
      <td>Emperor</td>
      <td>Irritable</td>
      <td>Psychic</td>
   </tr>
   <tr>
      <td>Isis</td>
      <td>She of Life and Death</td>
      <td>Priestess</td>
      <td>Irritable</td>
      <td>Psychic</td>
   </tr>
   <tr>
      <td>Anubis</td>
      <td>Bearer of the Scales</td>
      <td>Judgement</td>
      <td>Irritable</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Andras</td>
      <td>Menacing Owlman</td>
      <td>Devil</td>
      <td>Timid</td>
      <td>Fire, Bless</td>
   </tr>
   <tr>
      <td>Mot</td>
      <td>Coffin-borne God</td>
      <td>Death</td>
      <td>Gloomy</td>
      <td>Wind</td>
   </tr>
</table>

##### Okumura's Palace

<table>
   <tr>
      <th>Persona</th>
      <th>Shadow</th>
      <th>Arcana</th>
      <th>Personality</th>
      <th>Weakness</th>
   </tr>
   <tr>
      <td>Decarabia</td>
      <td>Vicious Pentagram</td>
      <td>Councillor</td>
      <td>Timid</td>
      <td>Physical</td>
   </tr>
   <tr>
      <td>Black Ooze</td>
      <td>Pulsing Mud</td>
      <td>Moon</td>
      <td>Timid</td>
      <td>Electric, Psychic, Bless</td>
   </tr>
   <tr>
      <td>Arahabaki</td>
      <td>Awakened God</td>
      <td>Hermit</td>
      <td>Gloomy</td>
      <td>Psychic, Nuclear</td>
   </tr>
   <tr>
      <td>Girimehkala</td>
      <td>Rebellious Elephant</td>
      <td>Moon</td>
      <td>Irritable</td>
      <td>Bless</td>
   </tr>
   <tr>
      <td>Mothman</td>
      <td>Vampire Moth</td>
      <td>Moon</td>
      <td>Timid</td>
      <td>Gun</td>
   </tr>
   <tr>
      <td>Belphegor</td>
      <td>Ambassador of Filth</td>
      <td>Tower</td>
      <td>Timid</td>
      <td>Fire</td>
   </tr>
   <tr>
      <td>Lilim</td>
      <td>Woman Who Brings Ruin</td>
      <td>Devil</td>
      <td>Gloomy</td>
      <td>Wind, Bless</td>
   </tr>
   <tr>
      <td>Mithras</td>
      <td>Dark Sun</td>
      <td>Sun</td>
      <td>Gloomy</td>
      <td>Psychic</td>
   </tr>
   <tr>
      <td>Kaiwan</td>
      <td>Wishless Star</td>
      <td>Star</td>
      <td>Timid</td>
      <td>Nuclear</td>
   </tr>
   <tr>
      <td>Thunderbird <span class="badge badge-danger">Royal</span></td>
      <td>Storm-Invoking Ptarmigan</td>
      <td>Sun</td>
      <td>Upbeat</td>
      <td>Psychic, Curse</td>
   </tr>
   <tr>
      <td>Kumbhanda</td>
      <td>Life-Draining Spirit</td>
      <td>Hermit</td>
      <td>Gloomy</td>
      <td>Psychic</td>
   </tr>
</table>

##### Niijima's Palace

<table>
   <tr>
      <th>Persona</th>
      <th>Shadow</th>
      <th>Arcana</th>
      <th>Personality</th>
      <th>Weakness</th>
   </tr>
   <tr>
      <td>Ose</td>
      <td>Cruel Leopard</td>
      <td>Fool</td>
      <td>Irritable</td>
      <td>Bless</td>
   </tr>
   <tr>
      <td>Unicorn</td>
      <td>Expressionless Beast</td>
      <td>Faith</td>
      <td>Timid</td>
      <td>Curse</td>
   </tr>
   <tr>
      <td>Kikuri-Hime</td>
      <td>Mountain Girl</td>
      <td>Priestess</td>
      <td>Timid</td>
      <td>Fire</td>
   </tr>
   <tr>
      <td>Valkyrie</td>
      <td>Funerary Warrior</td>
      <td>Strength</td>
      <td>Irritable</td>
      <td>Fire</td>
   </tr>
   <tr>
      <td>Power</td>
      <td>Divine Warrior</td>
      <td>Justice</td>
      <td>Irritable</td>
      <td>Curse</td>
   </tr>
   <tr>
      <td>Ganesha</td>
      <td>Auspicious Pachyderm</td>
      <td>Sun</td>
      <td>Irritable</td>
      <td>Psychic</td>
   </tr>
   <tr>
      <td>Queen Mab</td>
      <td>Midnight Queen</td>
      <td>Magician</td>
      <td>Gloomy</td>
      <td>Wind</td>
   </tr>
   <tr>
      <td>Kushinada-Hime</td>
      <td>Lamenting Sacrifice</td>
      <td>Lovers</td>
      <td>?</td>
      <td>Ice, Nuclear</td>
   </tr>
   <tr>
      <td>Rangda</td>
      <td>Dancing Witch</td>
      <td>Magician</td>
      <td>Gloomy</td>
      <td>Electric, Bless</td>
   </tr>
   <tr>
      <td>Skadi</td>
      <td>Quaking Lady of Shadow</td>
      <td>Priestess</td>
      <td>Irritable</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Norn</td>
      <td>Final Assessor</td>
      <td>Fortune</td>
      <td>Upbeat</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Jatayu <span class="badge badge-danger">Royal</span></td>
      <td>Arrogant Vulture</td>
      <td>Hanged Man</td>
      <td>Irritable</td>
      <td>Nuclear</td>
   </tr>
   <tr>
      <td>Raja Naga</td>
      <td>Snake King</td>
      <td>Temperance</td>
      <td>?</td>
      <td>None</td>
   </tr>
</table>

##### Shido's Palace

<table>
   <tr>
      <th>Persona</th>
      <th>Shadow</th>
      <th>Arcana</th>
      <th>Personality</th>
      <th>Weakness</th>
   </tr>
   <tr>
      <td>Cerberus</td>
      <td>Guard Dog of Hades</td>
      <td>Chariot</td>
      <td>Irritable</td>
      <td>Ice</td>
   </tr>
   <tr>
      <td>Dakini</td>
      <td>Blood-thirsty Demoness</td>
      <td>Empress</td>
      <td>Upbeat</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Sarasvati</td>
      <td>Strumming Veena Player</td>
      <td>Priestess</td>
      <td>Gloomy</td>
      <td>Nuclear</td>
   </tr>
   <tr>
      <td>Narcissus</td>
      <td>Self-Infatuated Star</td>
      <td>Lovers</td>
      <td>Timid</td>
      <td>Fire</td>
   </tr>
   <tr>
      <td>King Frost</td>
      <td>Monarch of Snow</td>
      <td>Emperor</td>
      <td>Upbeat</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Titania</td>
      <td>Scandalous Queen</td>
      <td>Empress</td>
      <td>Upbeat</td>
      <td>Psychic</td>
   </tr>
   <tr>
      <td>Parvati</td>
      <td>Destructive Beauty</td>
      <td>Lovers</td>
      <td>Timid</td>
      <td>Curse</td>
   </tr>
   <tr>
      <td>Barong</td>
      <td>Dancing Lion</td>
      <td>Emperor</td>
      <td>?</td>
      <td>Wind, Curse</td>
   </tr>
   <tr>
      <td>Forneus</td>
      <td>Rhetorician of the Sea</td>
      <td>Magician</td>
      <td>Gloomy</td>
      <td>Electric</td>
   </tr>
   <tr>
      <td>Hanuman</td>
      <td>Nimble Monkey King</td>
      <td>Strength</td>
      <td>Upbeat</td>
      <td>Ice</td>
   </tr>
   <tr>
      <td>Garuda</td>
      <td>Raging Bird God</td>
      <td>Star</td>
      <td>?</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Baphomet</td>
      <td>Heretic Goat</td>
      <td>Devil</td>
      <td>?</td>
      <td>Bless</td>
   </tr>
   <tr>
      <td>Oberon</td>
      <td>Unfaithful Dream-King</td>
      <td>Emperor</td>
      <td>Irritable</td>
      <td>Nuclear</td>
   </tr>
   <tr>
      <td>Atavaka <span class="badge badge-danger">Royal</span></td>
      <td>Infuriated Wisdom King</td>
      <td>Faith</td>
      <td>Irritable</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Ongyo-Ki</td>
      <td>Shadow Cleaner</td>
      <td>Hermit</td>
      <td>?</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Kali</td>
      <td>The Blackened Fury</td>
      <td>Empress</td>
      <td>Irritable</td>
      <td>None</td>
   </tr>
</table>

##### Depths of Mementos

<table>
   <tr>
      <th>Persona</th>
      <th>Shadow</th>
      <th>Arcana</th>
      <th>Personality</th>
      <th>Weakness</th>
   </tr>
   <tr>
      <td>Lilith</td>
      <td>Harlot of Desire</td>
      <td>Moon</td>
      <td>?</td>
      <td>Fire</td>
   </tr>
   <tr>
      <td>Moloch</td>
      <td>Sacrificial Pyrekeeper</td>
      <td>Hanged Man</td>
      <td>Upbeat</td>
      <td>Ice</td>
   </tr>
   <tr>
      <td>Nebiros</td>
      <td>Wandering Reviver</td>
      <td>Devil</td>
      <td>?</td>
      <td>Bless</td>
   </tr>
   <tr>
      <td>Dionysus</td>
      <td>Hedonistic Braggart</td>
      <td>Councillor</td>
      <td>Upbeat</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Melchizedek</td>
      <td>Pagan Savior</td>
      <td>Justice</td>
      <td>Irritable</td>
      <td>Wind</td>
   </tr>
   <tr>
      <td>Chernobog</td>
      <td>The Black Avenger</td>
      <td>Death</td>
      <td>?</td>
      <td>Fire, Bless</td>
   </tr>
   <tr>
      <td>Baal</td>
      <td>Reviled Dictator</td>
      <td>Emperor</td>
      <td>Upbeat</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Thor</td>
      <td>Thunder Emperor</td>
      <td>Chariot</td>
      <td>Upbeat</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Yamata-no-Orochi</td>
      <td>Drunken Serpents</td>
      <td>Judgement</td>
      <td>?</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Belial</td>
      <td>Missionary of Depravity</td>
      <td>Devil</td>
      <td>?</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Mara</td>
      <td>Throbbing King of Desire</td>
      <td>Tower</td>
      <td>?</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Abaddon</td>
      <td>Abyssal King of Avarice</td>
      <td>Judgement</td>
      <td>?</td>
      <td>None</td>
   </tr>
</table>

##### Qliphoth World

<table>
   <tr>
      <th>Persona</th>
      <th>Shadow</th>
      <th>Arcana</th>
      <th>Personality</th>
      <th>Weakness</th>
   </tr>
   <tr>
      <td>Dominion</td>
      <td>Merciless Inquisitor</td>
      <td>Justice</td>
      <td>Timid</td>
      <td>Electric</td>
   </tr>
   <tr>
      <td>Uriel</td>
      <td>Herald of Death</td>
      <td>Justice</td>
      <td>?</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Raphael</td>
      <td>Cleanser of Heaven</td>
      <td>Lovers</td>
      <td>?</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Gabriel</td>
      <td>Declarer of Anguish</td>
      <td>Temperance</td>
      <td>?</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Michael</td>
      <td>Apocalyptic Guide</td>
      <td>Judgement</td>
      <td>?</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Crystal Skull</td>
      <td>Treasure Demon</td>
      <td>Fool</td>
      <td>?</td>
      <td>Wind</td>
   </tr>
   <tr>
      <td>Throne</td>
      <td>Fire Assassin</td>
      <td>Justice</td>
      <td>Gloomy</td>
      <td>Nuclear</td>
   </tr>
</table>

##### Maruki's Palace <span class="badge badge-danger">Royal</span>

<table>
   <tr>
      <th>Persona</th>
      <th>Shadow</th>
      <th>Arcana</th>
      <th>Personality</th>
      <th>Weakness</th>
   </tr>
   <tr>
      <td>Orichalcum</td>
      <td>Treasure Demon</td>
      <td>Faith</td>
      <td>?</td>
      <td>Bless</td>
   </tr>
   <tr>
      <td>Bugs</td>
      <td>Killer Teddy Bear</td>
      <td>Fool</td>
      <td>?</td>
      <td>Nuclear</td>
   </tr>
   <tr>
      <td>Byakhee</td>
      <td>Evil Synthetic Organism</td>
      <td>Moon</td>
      <td>Gloomy</td>
      <td>Ice, Nuke</td>
   </tr>
   <tr>
      <td>Loa</td>
      <td>Dream-Dwelling Skull</td>
      <td>Hermit</td>
      <td>?</td>
      <td>Psychic, Bless</td>
   </tr>
   <tr>
      <td>Cu Chulainn</td>
      <td>Brave Spear-Bearer</td>
      <td>Faith</td>
      <td>?</td>
      <td>Electric</td>
   </tr>
   <tr>
      <td>Dionysus</td>
      <td>Hedonistic Braggart</td>
      <td>Councillor</td>
      <td>Upbeat</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Macabre</td>
      <td>Dancer of Death</td>
      <td>Hanged Man</td>
      <td>Gloomy</td>
      <td>Bless</td>
   </tr>
   <tr>
      <td>Chimera</td>
      <td>Deformed Lion God</td>
      <td>Strength</td>
      <td>?</td>
      <td>Wind, Curse</td>
   </tr>
   <tr>
      <td>Nebiros</td>
      <td>Wandering Reviver</td>
      <td>Devil</td>
      <td>Upbeat</td>
      <td>Bless</td>
   </tr>
   <tr>
      <td>Scathach</td>
      <td>The Shadowed One</td>
      <td>Priestess</td>
      <td>?</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Fafnir</td>
      <td>Evil Voracious Dragon</td>
      <td>Hermit</td>
      <td>Irritable</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Alilat</td>
      <td>Decadent False God</td>
      <td>Empress</td>
      <td>?</td>
      <td>Fire, Curse</td>
   </tr>
   <tr>
      <td>Baal</td>
      <td>Reviled Dictator</td>
      <td>Emperor</td>
      <td>Upbeat</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Belial</td>
      <td>Missionary of Depravity</td>
      <td>Devil</td>
      <td>?</td>
      <td>None</td>
   </tr>
   <tr>
      <td>Hastur</td>
      <td>Warped Abyss</td>
      <td>Star</td>
      <td>Irritable</td>
      <td>None</td>
   </tr>
</table>

##### Mementos

<table>
   <tr>
      <th>Persona</th>
      <th>Shadow</th>
      <th>Arcana</th>
      <th>Personality</th>
      <th>Weakness</th>
   </tr>
   <tr>
      <td>Regent</td>
      <td>Treasure Demon</td>
      <td>Emperor</td>
      <td>?</td>
      <td>Nuclear</td>
   </tr>
   <tr>
      <td>Slime</td>
      <td>Viscid Rotting Meat</td>
      <td>Chariot</td>
      <td>Timid</td>
      <td>Fire, Wind</td>
   </tr>
   <tr>
      <td>Kodama</td>
      <td>Wavering Tree Spirit</td>
      <td>Star</td>
      <td>Upbeat</td>
      <td>Fire</td>
   </tr>
   <tr>
      <td>Obariyon</td>
      <td>Piggyback Demon</td>
      <td>Fool</td>
      <td>Irritable</td>
      <td>Electric</td>
   </tr>
   <tr>
      <td>Pisaca</td>
      <td>Corpse-eating Corpse</td>
      <td>Death</td>
      <td>?</td>
      <td>Fire, Bless</td>
   </tr>
   <tr>
      <td>Sudama</td>
      <td>Noisy Mountain Spirit</td>
      <td>Hermit</td>
      <td>Timid</td>
      <td>Ice, Nuclear</td>
   </tr>
   <tr>
      <td>Queen's Necklace</td>
      <td>Treasure Demon</td>
      <td>Empress</td>
      <td>?</td>
      <td>Psychic</td>
   </tr>
   <tr>
      <td>Choronzon</td>
      <td>Gathering Devil</td>
      <td>Magician</td>
      <td>Timid</td>
      <td>Bless</td>
   </tr>
   <tr>
      <td>Sandman</td>
      <td>Envoy of Slumber</td>
      <td>Magician</td>
      <td>Upbeat</td>
      <td>Fire, Electric</td>
   </tr>
   <tr>
      <td>Legion</td>
      <td>Fused Ghost</td>
      <td>Fool</td>
      <td>Timid</td>
      <td>Bless</td>
   </tr>
</table>