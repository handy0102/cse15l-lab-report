# Lab Report 3

I'll be using the **grep** command :D.

All my examples came from https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix

## grep -r "string" file-name/directory
**EX1)**

Input:
`
andyho@Andys-MacBook-Air Abernathy % grep -r "In the late 1940s"`

Output:
`./ch1.txt:In the late 1940s, Bond Stores, the largest men’s clothing chain at the time, created a sensation in New York City by offering a wide selection of suits with two pairs of pants instead of one, reintroducing a level of product choice not seen since before the war.1 When the line of hopeful buyers at its Times Square store stretched around the block, Bond had to impose a limit of two suits per customer. During World War II, the apparel and textile industries had been converted to supply field jackets, overcoats, and uniforms to the U.S. and Allied Forces. But in the years immediately following the war, returning soldiers, the end of rationing, and pent-up customer demand meant apparel was in short supply.`

Explanation:
This command takes in the string pattern "In the late 1940s". It then recursively searches in the current directory (Abernathy) and its subdirectories for exact matches and outputs the lines that contain the match along with the file name. This is useful for looking for specific data inside big data files. 

**EX2)** 

Input: 
`andyho@Andys-MacBook-Air written_2 % grep -r "no matching string"`

Output:
No output :(

Explanation:
This command takes in the string pattern "no matching string". It searches for a line with the matching string, but it does not find any. This is useful for checking if specific patterns exist in a data file.

## grep -c "string" file-name

**EX1)**

Input: 
`andyho@Andys-MacBook-Air berlitz2 % grep -c "Bahamas" Bahamas-History.txt`

Output:
`23`

Explanation:
This command takes in a string pattern "Bahamas" and returns the number of lines that contain that string inside Bahams-History.txt. This command is useful for checking if the string pattern is a common occurance in a text file.

**EX2)**

Input:
`andyho@Andys-MacBook-Air berlitz2 % grep -c "Not Bahamas" Bahamas-History.txt`

Output:
`0`

Explanation:
Takes in the string "Not Bahamas" and counts the number of lines that pattern appears. In this case it's zero, because no line in that file contains it. This is useful for confirming if there is no sentence/word that appears in the text file.

## grep -v "string" file-name

**EX1)**

Input:
`andyho@Andys-MacBook-Air berlitz2 % grep -v "Bahamas" Bahamas-history.txt` 

Output:
`A Brief History
Colonization and Piracy
In 1670 six Lords Proprietors of Carolina were granted the Bahama islands by Charles II, but for nearly 50 years their weak governors on New Providence either couldn’t or wouldn’t suppress the piracy raging through the archipelago. Then, in 1684, to avenge countless raids against their ships, the Spanish dispatched a powerful squadron from Cuba to attack Nassau. This sent the majority of the English settlers fleeing to Jamaica or Massachusetts, but didn’t have much effect on the pirates.
New Providence knew some spells of prosperity in the mid-18th century as privateering resumed with England at war with Spain. The town of Nassau expanded, and improvements were made between 1760 and 1768 by another revered governor, William Shirley from Massachusetts.
The American Revolutionary War
Emancipation and Decline
Nassau became a free port in 1787, sparking a surge in trading activity. Loyalists built a number of the attractive colonial-style homes and public buildings still standing today, and during the War of 1812, privateers enjoyed another profitable spell against American vessels.
Civil War Blockade Running
For a time a new fiber called sisal seemed promising. But Bahamian soil was too poor and Mexico grew a better plant. Neville Chamberlain, future British Prime Minister, took over his family’s sisal operation on Andros in the 1890s. It failed, the natives said, because of that island’s evil elves called chickcharnies, who cast a spell on the family for disturbing the land. Hopes were raised, and also fizzled, over Bahamian citrus and pineapple. Sponging, another vitally important industry at the end of the 19th century, also had setbacks. A hurricane in 1839 drowned some 300 sponge fishermen in the ‘mud’ off Andros, and a devastating fungus some 40 years later killed almost all the sponges.
The 20th Century
Desperate for work, perhaps 20 percent of the Bahamian population left to take construction jobs in Florida between the turn of the century and World War I. During that war hundreds of Bahamians saw active service with British forces. The islands suffered food shortages and a serious bank failure, but nothing more threatening militarily than rumors of German submarines offshore.
Liquor money bought Nassau better houses, churches, lighting, water, roads, sewers, docks, and hotels. The city’s first gambling casino opened in 1920; the first daily air service from Miami began in 1929; the yacht set decided Nassau was fashionable, and many wealthy Americans as well as Prohibition millionaires built homes on the islands.
Then, to the astonishment of the local populace, the Duke of Windsor, having given up his throne for an American divorcée, was named governor of the little colony in 1940. He and the Duchess remained until 1945.`

Explanation:
This command basically returns all the lines from Bahamas-History.txt that don't contain the string "Bahamas". This is really useful for people who are allergic to the word "Bahamas", but still want to read an article on the Bahamas. Idk maybe Sam Bankman stole their money.

**EX2)**

Input:
`andyho@Andys-MacBook-Air berlitz2 % grep -v "Handicraft" Cancun-WhatToDo.txt`

Output: 
`What to Do
Shopping
Where to Shop
Traveling around the Yucatán peninsula will present you with a wealth of shopping opportunities — many are only a short stroll away from the beaches. Cancún has a number of modern, air-conditioned shopping malls, with internationally recognized brand names, where you can shop in comfort from morning to night, though of course prices are higher here than inland.
For strolling and browsing in the Mexican sunshine or the cooler air of the evening, there are shopping streets in San Miguel de Cozumel, Isla Mujeres, and in Calle 5 in Playa del Carmen. These streets have shops selling locally produced crafts and imported goods, pretty boutiques, and jewelry stores.
Visit the Hi Kuic craft market in downtown Cancún, and better still the Mercado Municipal in Mérida, to experience the genuine, colorful atmosphere of a Mexican market. Examples of every locally produced craft can be found in abundance here, and you’ll shop cheaper than in the resorts, especially if you practice your bartering skills beforehand.
Don’t let the range of goods blind you to low quality or fakes. Always examine the item you want very carefully and shop around to get a feel of the prices before you buy. Most shops in the main tourist areas will stay open until 9 or 10pm. Prices will often be quoted, and you will be able to pay, in US dollars.
What to Buy
Weaving has also been a very important skill for the Mayans. The fabric produced on personal looms in traditional patterns and colors is used in a variety of different products. Sarapes, cotton or wool blankets, and rugs are popular, but you will also find the material made into jackets and hats.
Mayan themes. The Maya have a special place in the imagination — perhaps only surpassed by the ancient Egyptians — and their traditional motifs and copies of their ceremonial artifacts make popular souvenirs. Carvings of the gods, Chaac Mool in particular, along with revered creatures such as the jaguar or the feathered serpent, are produced in stone, onyx, silver, wood, and papier-mâché, in various sizes from lucky talisman for your purse to sculpture for your garden.
Ceremonial masks are also very beautiful and can be found in a range of qualities and sizes. Made from papier-mâché that is smoothed and brightly painted, they make beautiful wall decorations.
Pottery and glassware. Terracotta pots have been the basic cooking utensil for generations of Mayan families. You’ll find these in various sizes and with different decoration. Blown glassware is also exquisite; bowls, jugs and vases, and glasses can be bought throughout the region.
Silver. Mexico is still one of the largest producers of silver in the world, despite the Spanish conquistadors having looted tons of it during their years of conquest. There is an amazing range of jewelry available, such as chains, earrings, and finger and toe rings, and prices are extremely competitive. Larger pieces such as tea-sets and goblets can be found in the bigger stores, as can silver pill-boxes, purses, or small “sombreros.” Always make sure that your purchase bears a stamp of the word Mexico and of the numbers 925 (the standard quality of silver found here) or 960 (purer but slightly softer). This ensures that you are buying genuine silver and not a cheap alloy.
Tequila and other alcohol. Tequila is the national drink of Mexico, made from the distilled juice of the agave plant (100% agave tequila is the best quality), and it can be bought under numerous trade names. It is produced only in a very small region of Mexico, around the town of Tequila near Guadalajara, and is in reality a refined version of the agave drink Mezcal. You can also take home a bottle of the Yucatecan liquor Xtebentun, with its flavor of anise, honey, and flowers.
Clothing. You are sure to find something that fits your personal taste in summer attire in the Yucatán. Designer labels from the US and Europe are abundant in the tourist-zone malls in Cancún. Smaller stores throughout the region are filled with attractive beachwear, T-shirts, hats, footwear, and cool, comfortable cotton dresses, skirts, and sarongs that are ideal for the warm climate here.
Locally produced cottons and woven garments are sold in craft-markets and stores. The colorful patterns have been handed down through the generations. In the countryside, the Mayan women still wear the traditional huipile, a loose cotton slip with embroidered detail; the everyday version has stitching around the neckline and hem, the ceremonial version several layers of embroidery and lace. In Mérida, the men wear the guayabera, a short-sleeved linen or cotton shirt with finely pleated front detail, worn untucked. These tend to be much cooler than fitted shirts. Huaraches are hand-fashioned leather sandals with sisal thongs. You can top off your whole traditional ensemble with a hat: local people wear good quality panama hats (many imported from Guatemala). You can also buy sombreros, though these are actually traditional in regions of Mexico other than Yucatán.
Duty-Free Shopping
Cozumel is a major cruise destination and as such offers goods like fragrances and gemstones at duty-free prices. You can buy loose stones or finished pieces at a number of large, air-conditioned stores on Avenida Melgar, with prices said to be as much as 40% lower than US retail. If you intend to make a major purchase of this type while visiting the region, it would be wise to research the prices and quality of goods at home, before you travel, so that you can be sure you are getting a good deal.
Sports
Diving
Cancún, Cozumel, and the Maya Riviera offer some of the most pristine waters for diving and a wealth of natural reefs and artificial dive sites to explore. They are still considered some of the best sites in the world, despite the explosion in the number of divers over the last two decades. The lack of soil and rivers on the Yucatecan mainland mean that there is no silt in the sea to reduce underwater visibility, and there is little heavy industry in the area to pollute the ocean, leaving the marine life relatively healthy.
The island of Cozumel is still regarded as the jewel among diving areas. There are 30 km (20 miles) of reef, at many different depths, off the western coast. Divers have a chance to see turtles, sharks, and barracuda in their natural environment; the warm waters make for exciting and comfortable diving throughout the year. Plus, there are opportunities for both certified divers and those who would like to earn their certification.
Cancún is a great beginner’s resort; it has many shallow dive sites suitable for the novice. Experts can be well rewarded too — just a short distance from your hotel are challenging dive sites and some of the richest marine life anywhere on earth.
Remember to bring your dive certificate, as you will only be allowed to rent equipment and dive if you can prove your competence.
If you want to learn to dive in Cancún and Cozumel, there is an excellent network of dive centers offering training to professional levels. All centers are affiliated with one of the major certifying bodies, NAUI (National Association of Underwater Instructors) or PADI (Professional Association of Diving Instructors), the latter being the most common. The basic qualification, the Open Water certificate, takes five days to complete. Upon completion you can dive with an instructor to a depth of 18 m (60 ft), which opens to you many sites in the region. Diving centers also offer an introductory session known as the “Discover Scuba Program,” which includes a morning or afternoon of theory and swimming-pool work to give you the chance to practice the basic techniques. Many large hotels offer this lesson as a facility for their guests.
The following are two reputable local dive centers: Diving Adventures, Calle 5 Sur #22, Cozumel; Tel. 87/2-3009; <www.divingadventures.net>. Scuba Cancún, km 5 Paseo Kukulkán, lagoon side, Cancún; Tel. 98/83-1011; fax 98/84-2336.
It is also possible to dive and swim in cenotes, sinkholes found in the sub-surface limestone layer of the Yucatán peninsula, caused by millions of years of erosion. The Maya considered them to be holy places because they were the only source of fresh water other than what fell from the sky; for this reason, Mayan artifacts have been found in many cenotes. The holes provide an environment for turtles, eels, and a variety of tropical fish. Swimming in the cool, fresh water of the cenotes (a nice change from the salt water of the sea) is great fun. Cenote diving is only for the experienced. Always go through a reputable dive company; the companies listed above will offer further advice.
Snorkeling
Well over half of all visitors to the region will snorkel while on vacation. The superb clarity and warmth of the water, the abundant sea life even in the shallows, and the proximity of all of this to the resorts are what make snorkeling here appealing. You can snorkel at just about every beach on the west coast of Cozumel, on Isla Mujeres, and along the Maya Riviera.
The many national parks offer more natural environments, though the sea may still be crowded with fellow snorkelers during the high season. Garrafón/Punta Sur Park on Mujeres and Chankanaab National Park on Cozumel both rent snorkeling equipment.
The numerous coves (narrow bays with rocky walls found all along the coastline), are a perfect environment for small, brightly colored tropical fish. Xcaret is probably the most famous site, but you can enjoy snorkeling at Xel-Ha and Trés Rios as well.
Not yet qualified to dive? Both SNUBA and BOB are half-and-half water experiences. With both you are underwater, but with a constant supply of air from tubes at the surface. BOB, the Breathing Observation Bubble, is a kind of underwater scooter with oxygen helmet. Contact Hotel Cancún Marina Club, km 5.5 (Tel. 98/83-4440), for details. With SNUBA you wear a helmet, but you walk on the ocean floor. Contact AquaWorld in Cancún for further details.
Other Activities
Swim with the dolphins. These programs exist at various locations around the region, so you will have the opportunity no matter which of the big resorts you choose. Some venues have a range of different programs, from simply free-swimming with dolphins, to performing exercises with them, to helping a trainer for a day. Dolphin Discovery operates programs at Isla Mujeres, Cozumel, and Puerto Aventuras; <www.dolphindiscovery.com>. Other programs can be found at Xcaret; Tel. 98/83-3143; fax 98/83-3324.
Viewing marine life without getting wet. If getting into the water isn’t for you, then take a glass-bottom boat ride; trips navigate the mangrove swamps or venture out to the ocean reefs. It is also possible to travel under the surface of the water in a submersible craft. Nautibus, Sub See Explorer, and Atlantis XII all submerge to 50 m (150 ft) to explore the reef eco-system. Nautibus has four sailings a day: El Embarcadero, km 4 Cancún Hotel Zone; Tel. 98/83-3732. AquaWorld boasts various craft as well — they can be found at Kukulkán Boulevard, km 15.2 Hotel Zone; Tel. 98/85-2288; fax 98/85-2299; <www.aquaworld.com.mx>. Atlantis Submarine: Chankanaab km 4, Casa del Mar Hotel, Cozumel; Tel. 987/2-5671 or (888) REAL-SUB (toll-free in the US); <www.goatlantis.com>.
Watersports. Most of the major resorts will have water “toys” for rent; you can jet-ski or water-bike in the Caribbean or along the Mangrove swamps in the lagoon at Cancún. Note: Do obey the speed limits, in place to protect the delicate environment which is damaged by waves from speeding boats and jet-skis. And what better way to view the beautiful landscape, particularly the long beach and lagoon at Cancún, than from a parasail some 33 m (100 ft) up in the air? You’ll be able to fully appreciate the color of the sand and the ocean from on high.
Sport fishing. The warm waters of the Caribbean are teeming with fish, and sport fishing is becoming increasingly popular. Bonito, amberjack, barracuda, and shark can be caught in these waters all year; huge sailfish, tuna, and several species of marlin are most common between March and June; and in the winter months shoals of grouper and jewfish abound. Large, powerful boats can be organized at just about every resort along the coast — they are particularly plentiful in Cozumel and Playa del Carmen. The local guides are especially experienced and helpful.
Prices vary, but a full day’s rental of boat and crew (up to six passengers) is between $400–500. Half-day rentals are also available. Ocean Tours in San Miguel is just one boat-charter company; Tel. 987/2-1379; fax 987/2-3459; e-mail: <ocean@cozumel.czm.com.mx>.
The region also hosts a number of fishing tournaments.
Golf. Cancún is the site for a growing number of golf courses, and the climate of the area is ideal for a round or two. Pok-Ta-Pok was the first course, and some still say the best. However, since it opened, several large hotels have built courses as part of their guest facilities: The Meliá Cancún, km 15; The Hilton Cancún, km 17; and The Westin Regina, km 19.5. There are several courses along the Maya Riviera, principally at Puerto Aventuras, and Playacar courses are located in Playa del Carmen.
Horseback riding. The Spanish introduced horses to the region; they were perfect for transport through the “low jungle.” Today you can explore the area on horseback, enjoying organized and guided trails at many parks, such as Xcaret and Trés Rios. All across the region you will see ranches advertising their services — often you will see a horse tied in the shade at the ranch entrance to indicate that riding is offered.
Entertainment
Once the sun goes down, Cancún gears up. There’s no shortage of places to go or things to do, and no need to take a long novel to fill those quiet moments — there just won’t be any. Many people don’t take to their beds until they’ve seen the sun come up. If you choose to stay in Mujeres or Cozumel, things will be a bit more laid back. The diving fraternity tends to enjoy low-key, less glamorous entertainment and relatively early nights before they head under the waves early the following day.
Before you head straight into the resort atmosphere of Cancún, check out what’s happening in your hotel. Many have “Las Vegas style” floor shows, Mexican evenings with traditional folk music and dances, and clubs where you can take to the dance floor yourself.
Cancún is developing so quickly that the latest hot-spots change constantly. Ask your concierge where the place to be is, or just follow the crowds along the strip. Paseo Kukulkán in downtown Cancún has a collection of bars and clubs. On weekends you can join the locals in the Parque de Palapas, where the strains of rock, salsa, and folk music can blend together into a bewildering cacophony. But this doesn’t prevent everyone from having great fun — and the atmosphere is definitely infectious.
Cozumel has a number of music bars along Avenida Melgar and in the downtown region. All the large hotels have an entertainment program and a nightclub on site.
Fiestas
The Spanish colonists carried on the traditions of their mother country, and to this day there are yearly fiestas in most major towns. Many mark Saint’s days or founding days, and the whole population will dress up and enjoy lots of singing and dancing. Most have a religious procession to start the proceedings. The major fiestas are listed in the Calendar of Events (see page 92), but ask the tourist information office about what’s going on during your stay.
The city of Mérida seems to be in the throes of a constant fiesta, hosting live cultural shows at sites around the downtown area. Here you will find the most authentic cultural displays in the region. The program changes nightly from ballet to traditional Yucatecan folk music and dances, and all the performances are free. There are special performances on the famed Mérida Domingos (Mérida Sundays), lasting all day but for a short break in the heat of the afternoon, and coinciding with a huge market. On Sunday evenings Mexican families take to the streets to meet friends and family, dance, and generally have a good time.
Attractions for Children
Mexicans love children, and will dote on yours. Kids are always welcome in restaurants and cafés. There are also many attractions and activities in the region to keep them happy.
Beaches. Children can play for hours with sand and water. The beaches on the western coast of Cozumel offer crystal-clear, warm water with generally benign conditions and a range of facilities such as restaurants, rest rooms, and lockers. Older children can enjoy snorkeling just offshore. Don’t forget to protect young skin from the sun, which can be extremely powerful here. Always have a sun protection product at hand, and a layer of clothing such as a T-shirt. The sun’s rays penetrate the water, so protection is needed when snorkeling also.
Submersible rides. Even very young children can safely see the fish and other marine life from inside a mini-submarine.
Boat trips. A day trip in a boat from Cancún to Isla Mujeres, or simply a trip around the coast or through the mangrove swamps can be a great adventure.
Dolphin Encounter. Older children can take to the water with these delightful marine mammals; younger children will enjoy watching the spectacle.
The caves at Loltún. These caves offer a relatively easy and safe introduction to the underground world. Some of the caverns are huge; the Mayan artifacts make it even more interesting.
Xcaret. Superb beach, swimming lagoon, safe snorkeling, animals, horseback riding, turtles, underground river, Mayan dances — what more would you need?
Calesa rides at Mérida and Izamal. Young and old alike enjoy touring the town in a small, horse-drawn buggy.
Fiesta celebrations. Youngsters will be very welcome at any Mexican celebration.
Wet’nWild in Cancún. Water slides and wave machines for those who can’t bear another moment at the beach!`

Explanation:
Like example 1, it returns all the lines inside the inputted file that contain the inputted string. Although it doesn't really look useful on this example, it would be very useful on data that don't have weird formatting like this. For example, if I don't care for handicraft, I can just remove most information pertaining to handicraft. 


## grep --color "string" file-name

I don't think markdown supports different colors so I take screen shots of the output. 

Input:


