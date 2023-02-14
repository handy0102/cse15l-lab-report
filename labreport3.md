# Lab Report 3

I'll be using the **grep** command :D.

All my examples came from https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix

## 1. grep -r "string" file-name/directory
**EXAMPLE 1)**

Input:
`
andyho@Andys-MacBook-Air Abernathy % grep -r "In the late 1940s"`

Output:
`./ch1.txt:In the late 1940s, Bond Stores, the largest men’s clothing chain at the time, created a sensation in New York City by offering a wide selection of suits with two pairs of pants instead of one, reintroducing a level of product choice not seen since before the war.1 When the line of hopeful buyers at its Times Square store stretched around the block, Bond had to impose a limit of two suits per customer. During World War II, the apparel and textile industries had been converted to supply field jackets, overcoats, and uniforms to the U.S. and Allied Forces. But in the years immediately following the war, returning soldiers, the end of rationing, and pent-up customer demand meant apparel was in short supply.`

Explanation:
This command takes in the string pattern "In the late 1940s". It then recursively searches in the current directory (Abernathy) and its subdirectories for exact matches and outputs the lines that contain the match along with the file name. This is useful for looking for specific data inside big data files. 

**EXAMPLE 2)** 

Input: 
`andyho@Andys-MacBook-Air written_2 % grep -r "no matching string"`

Output:
No output :(

Explanation:
This command takes in the string pattern "no matching string". It searches for a line with the matching string, but it does not find any. This is useful for checking if specific patterns exist in a data file.

## 2. grep -c "string" file-name

**EXAMPLE 1)**

Input: 
`andyho@Andys-MacBook-Air berlitz2 % grep -c "Bahamas" Bahamas-History.txt`

Output:
`23`

Explanation:
This command takes in a string pattern "Bahamas" and returns the number of lines that contain that string inside Bahams-History.txt. This command is useful for checking if the string pattern is a common occurance in a text file.

**EXAMPLE 2)**

Input:
`andyho@Andys-MacBook-Air berlitz2 % grep -c "Not Bahamas" Bahamas-History.txt`

Output:
`0`

Explanation:
Takes in the string "Not Bahamas" and counts the number of lines that pattern appears. In this case it's zero, because no line in that file contains it. This is useful for confirming if there is no sentence/word that appears in the text file.

## 3. grep -v "string" file-name

**EXAMPLE 1)**

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

**EXAMPLE 2)**

Input:
`andyho@Andys-MacBook-Air berlitz2 % grep -v -i "surf" bali-whattodo.txt`

Output:
`What to Do
Sports
At the top of the list of Bali’s great attractions are its beaches with the warm waters of the Indian Ocean lapping at the shores, but the range of active and sports choices is hardly limited to floating on the waves. The more unusual spectator sports include colorful water buffalo races (on Lombok) and, to the horror of many visitors, cockfighting, a local favorite on both Bali and Lombok, where it is sometimes carried on as part of religious ceremonies or festivals.
Watersports
Warm water, gorgeous coral, and vivid fish make for great snorkeling over the reefs, especially off the north coast of Bali, Nusa Lembongan, and Lombok’s offshore Gilis (see page 74). Take your own equipment if you have it. Otherwise, many hotels will lend or rent it to you — check the fit and condition carefully. Superb sites for SCUBA diving include Menjangan and Nusa Penida off Bali, and the Gilis. Specialist tour operators rent out all the equipment and run courses for complete beginners — make sure that the company you choose is licensed and that the instructors are fully qualified, with international certification.
Most resorts give you a number of swimming options. When the tide or sea conditions don’t suit, there is usually a pool. If there isn’t one where you are staying, you may be able to use another hotel’s pool for a small charge.
Whitewater rafting is one of the newer activities. Tour companies will pick you up at your hotel, then take you to the launch point on the Ayung river near Ubud, and provide you with the necessary equipment for an exhilarating trip. 
On Dry Land
Golf courses at Nusa Dua and up in the mountains at the Bali Handara Kosaido Country Club are both top-class, staging tournaments which bring some of the world’s best players. There’s a 9-hole course at Sanur, and at Lombok there is the 18-hole Suranadi course. Many hotels offer their own tennis courts, some floodlit for evening use. Air-conditioned squash courts are available at a few places. As the sun starts to set, informal soccer and volleyball games between visitors and locals begin on the beach at Kuta, Tuban, and Legian.
Walking in the countryside is one of the great pleasures of Bali. Don’t start at the southern resorts, which are a long way from the best scenery, but begin instead up in the hills, where it’s cooler. In Ubud, the Bina Wisata Information Center or your hotel can give you information on walks along the Campuan Ridge, or through picturesque local rice fields. Bookstores in Ubud sell detailed maps, including Bali Pathfinder and Ubud Surroundings, that will help guide you along country pathways. Keep Walking Tours (<balitrade@denpasar.wasantara.net.id>) at the Tegun Galeri shop in Jalan Hanoman offers one- to seven-hour guided walks; Victor Mason’s highly praised Bali Bird Walks (Tel. 0361 975 009) includes lunch, water, and use of binoculars. Both are very reasonably priced. At Munduk, in the beautiful mountains southwest of Lovina, Puri Lumbung Cottages (see page 134) offers an excellent program of walks, treks, and courses in local arts and crafts.
More arduous and serious mountain treks include climbing the active volcano Gunung Batur — a trek of several hours — and the crater rim and lake of Gunung Rinjani (on Lombok), which demands at least three days to complete.
Massage, both relaxing and therapeutic, is a Balinese tradition that many visitors have come to enjoy. The beaches are filled with men and women offering reasonably good massage at prices that are very low. Ubud has many good massage centers that offer very professional massage treatment, including mineral baths, all for approximately US$10; hotels and resorts offer similar treatment in more pampering surroundings for considerably more.
Spectator Sports
Regular buffalo races are held at Negara in western Bali, and on Lombok, with the normally sluggish beasts pulling decorated carts at surprising speeds. Kite-flying is a local obsession at Sanur and on the windswept Bukit Peninsula. You can buy beautiful, hand-painted kites at stands or from hawkers at Sanur and also at Kuta.
In Lombok, ritual fights long ago took the place of war. The Balinese and Sasaks hurl packets of cooked rice at each other in the October perang ketupet festival. Large crowds gather regularly in villages in Lombok to watch peresehan contests in which men armed with rattan canes and leather shields lash at each other until the referee declares one of them the victor.
Entertainment
Traditional Music, Puppetry, and Dance Performances
The sound of music in Bali can be the hypnotic tones of the gamelan orchestra, or the alluring call of the disco beat at Kuta or Legian, where the action begins at midnight and lasts until dawn. In the rest of the resorts, the nightlife is on a much smaller scale.
Bali’s own celebrated culture of dance and drama flourishes on two levels: for the visitors and for locals themselves. Ask at hotels, travel agencies, and tourist information offices to find out what is scheduled during your stay. They’ll probably point you towards some of the commercial performances put on in several villages, mostly in the Ubud area. Tickets (including transport) are sold at the tourist office in Ubud and by many of the tour operators. Increasingly, the culture is packaged and brought to you in shows staged at hotels. Some of these are of a very high standard: Dedicated dancers and musicians usually do give their best. But inevitably the atmosphere is different when they are performing for untutored tourists eating dinner, rather than for an expert village audience — and above all for their gods.
Drama and dance students will think that they’ve gone to heaven when they see the unique temple ceremonies. If you are invited, be prepared to wait for a long time. Starting times are highly elastic, and then some events will last for many hours. 
Many of the dances of Bali are also performed in western Lombok, either for the Balinese community there or, increasingly, for the tourists at Senggigi hotels. Lombok also has its own special dances, which are rarely staged commercially. Some are for men only — one simulating battle preparations probably derives from the Islamic tradition. The gandrung dance closely resembles Bali’s joged, in that a girl picks a male partner from the audience. Another group of dances is based on romantic legends from Sasak mythology, dating back to before the advent of Islam. Western-style nightlife is limited to Senggigi, where some hotels run discos and local groups play in the bar-restaurants.
The puppet shadow plays called wayang kulit (leather puppet) are not so often put on for tourists — the plots are too complex and the plays last too long (up to two days) for foreign consumption. A temple ceremony may give you a chance to join the audience for a while. You may look behind the screen — it’s permitted — to see the dalang or puppet master expertly controlling the beautiful figures, speaking all of their lines in a vast range of appropriate voices while conducting the small orchestra.
Dances of Bali
Legong: This is the visitors’ favorite dance, performed by three young girls: two principal dancers, the legongs, no more than 12 or 13 years old, and an attendant. Each is exquisitely dressed in glittering songket fabrics and wears a gilded and jeweled head-dress embellished with fresh frangipani (plumeria) flowers. The usual version (legong kraton) is the tale of a king and the princess he has abducted, performed by the two principals who, using various hand and facial gestures, portray the attempted seduction. 
Kecak: Part of a much longer ritual trance-dance which is called sanghyang, this is mostly performed separately. Up to 150 men in sarongs crouch in concentric circles around a flickering lamp and chant hypnotically while the story is acted out in the center of the circle. Taken from the Ramayana, the dance concerns Rama and Sita and the monkey armies of Hanuman and Sugriwa, hence the kecak’s popular title of “Monkey Dance.” The dance as performed today was choreographed by the German artist, Walter Spies, who did so much to influence art in the Ubud region during the 1930s.
Pendet: Six or more girls carrying trays of flower petals open the evening by scattering the petals over the stage as a symbol of welcome. At the same time, a man may light an incense-burning lamp. At temple ceremonies the pendet is danced to welcome the gods.
Janger: Twelve boys and twelve girls in groups of six form a square, the girls kneeling and swaying together to the music like reeds in the wind. The boys, wearing false moustaches, try to impress the girls as they strut and preen like fighting roosters.
Joged: A whole family of dances shares this name, performed to the music of an orchestra of bamboo xylophones and gongs. But one, properly called the jegog, has become so popular that it alone is often considered to be joged. A young woman dances alone at first, and then taps members of the audience in turn to dance with her. Try as they may to flirt or show off, she easily slips away from their advances. Few Westerners look anything but clumsy in comparison.
Barong: A mythical lion-like animal, the barong is covered in long hair and little mirrors. Animated by two men, it fights against the evil Rangda, queen of the witches. Her long claw-like fingernails hold a white cloth to hide her terrible face, bulging eyes, fangs, and flaming tongue while she advances on her victims. Allies of the barong, men wearing sarongs and each carrying a kris, try to attack Rangda but she puts them under a spell. In a trance, they turn the knives on themselves. Only the reappearance of the barong saves them.
In daily performances for visitors (each morning at Batubulan, for instance) the trances are inevitably simulated. Late at night in a village, however, you would see the wild-eyed men in a genuine frenzy or collapsing at the climax into unconsciousness, until revived by priests who sprinkle them with holy water.
Other Dances: Other performances you might see include scenes from the Hindu epic drama, the Ramayana, staged as a ballet. These may well be a showcase for fine dancing, gorgeous costumes, and the full range of the gamelan orchestra. In the topeng, the dancers are masked, meaning that they can convey character and emotion through movement alone. The stories are taken from Balinese history and mythology. 
Kebyar is the name of a group of solo dances of which the best known are performed by a seated man, using only the upper body. Baris is a vehicle for groups of young male dancers to display their command of technique, conveying a great range of emotions.
Festivals and Events
Most festivals are fixed by calendars different from the Western version (see page 91), so they change each year. Look for the Indonesian Directorate of Tourism’s annual Calendar of Events, which is published in Bali and gives dates and locations of temple festivals. Two celebrations stick to fixed dates: The Walter Spies festival in February and the summer Arts Festival, with superb performances, which is held in Denpasar in late June and early July.
Shopping
Bali produces a wide range and large quantity of crafts in every medium. Most of the decorative arts and crafts originally had a religious connection, as temple embellishments, offerings, or ceremonial dress. The land yielded plenty to eat without the need to work all day, every day, so people had time to create objects of beauty. The tradition continues, although production has been multiplied by the demand for souvenirs. Some craft shops in the villages have workshops attached, or you can watch the carvers, painters, or weavers in the adjoining compound.
In the past, nothing was expected to last: The climate and insects saw to that. So hardly anything is very old — “Antiques Made to Order” shop signs give the game away. 
Wood carvings: Dozens of villages devote themselves to Bali’s biggest craft business; Mas (see page 41) is the best-known, with hundreds of carvers and countless shops. Behind the scenes — but you may be invited for a visit — fathers pass on their skills to their sons, while the women do the polishing or painting. The best carvings are superb sculptures, but even the simplest, cheapest article can make an appealing souvenir. Among the massed garuda birds and masks, you’re bound to find something beautiful. 
The sign “Parasite Carvings” might puzzle you. A new idea, imported from the West, is to take the galls and other strange growths that occur on tree trunks and carve them into a witty or grotesque design, using the natural shape.
Jewelry: The village of Celuk (see page 40) specialized in producing silver and gold jewelry for centuries, so when tourism arrived, its position on the Denpasar-Ubud road was ideal. Dozens of tour buses stop at the big shops but there are many little workshops worth visiting, too. The smiths can produce any style: from intricate filigree work to simple bracelets. You don’t have to go to Celuk though, since every resort area has its share of shops. Silver should bear the “925” stamp of sterling silver (meaning it’s 92.5% pure).
Clothes and Fabrics: Bali is a huge bargain basement for a selection of beachwear, casual clothing, and, at a higher price but still excellent value, fashion designs. For the biggest choice of shops go to Kuta, and look for dresses, shirts, sarongs, and cover-ups in traditional batik fabric. 
Batik dyeing technique uses hot wax to draw or stamp a design on cloth before dipping it in the dye, so that the waxed areas are left undyed. The process can be repeated a number of times for greater complexity. Java is the source of the batik for dresses and sarongs sold in fashion shops; Balinese versions are usually much coarser. Hawkers will swear that their dress lengths of cheap printed cotton are batik. It’s easy to tell that they are not: Printed patterns don’t penetrate fully to the other side, while the real batik will show thin veins of color where the dye runs along tiny cracks in the wax (printed versions may try to simulate this). Real batik is always much more expensive. Used batik sarongs are highly prized, as their patterns are often no longer produced. Used batik can be bought for very low fixed prices at textile shops like Alec, on Jalan Legian in Kuta-Legian.
Endek or ikat fabrics, using threads dyed in patterns before weaving, come from Gianyar in Bali as well as other Indonesian islands. In Bali, only the weavers of Tenganan make grinsing, or double ikat, using pattern-dyed threads for both warp and weft. The genuine fabric is justifiably expensive — beware of fakes! You can find bold, primitive examples of ikat cloth, especially from islands such as Sumba, Flores, and Timor, in good textile shops.
Paintings: If you want a unique work of art, you’ll need to study the field. Visit the major collections to judge the standard of the best paintings, especially the Neka Museum and Museum Puri Lukisan in Ubud (see page 41) as well as the Arts Centre in Denpasar (see page 37). Don’t just assume that a high price guarantees original work.
And More… Look for the basketry from Bona, leather wayang kulit puppets from Puaya near Sukawati, and decorative umbrellas on roadside stalls east of Klungkung.
Shops take advantage of the tourist traffic to sell the products of other islands, too — embroidery and songket fabrics from Sumatra, primitive art from Irian Jaya, and silver from Sulawesi.
Lombok: Craft skills in Lombok tend to be devoted to household objects that can have a somewhat austere functional beauty. Look for the delicate, tightly-woven basketware, whether in mats, boxes, bowls, and bags, or the common Lombok souvenir of a model rice-barn. Painted wood boxes to store spices, tobacco, or jewelry are attractive. Simple red pottery comes from Penujak, and black pots from Rungkang are bound in an intricately woven basket.
Necessities: Some supermarkets and convenience stores have opened in Denpasar, such as Tiara Dewata, on Jalan Jenderal Sutoyo, with books, shoes, cosmetics, and even a playground for children and a swimming pool. There is a similar big shopping center near the airport, while smaller ones can be found in Kuta, Nusa Dua, Senggigi, and Lombok. In big towns, modern grocery shops, with big red “K” signs (Circle K) are open 24 hours a day and sell all kinds of necessities.
Bali FORCHILDREN
The Balinese treasure their children and yours will get the same treatment. Some resorts run children’s activity programs during the day, show videos in the early evening, and at night offer a babysitting service when you want to go off on your own. In losmen and homestay accommodations, the children of the owner’s family will probably want to make friends, and the older girls may offer to act as babysitters.`

Explanation:
Like example 1, it returns all the lines inside the inputted file that contain the inputted string. In this example, it helped me filter the lines with "surf" in it. I used -i so the captilization did not matter either. This command is useful for just filtering information that you find useless, like an activity that you've already done.


## 4. grep -n "string" file-name

**EXAMPLE 1)**

Input:
`andyho@Andys-MacBook-Air berlitz2 % grep -n "San Diego" California-WhereToGo.txt`

Output:
`7:Our journey begins with San Francisco and its nearby attractions and works its way down the coast to Los Angeles and San Diego before heading inland to the mountains and deserts of the Sierra Nevada and Death Valley. You can turn this itinerary upside down if you prefer, but either way, you should also consider making an excursion to Las Vegas, California’s favorite out-of-state playground.
136:San Diego
137:This is where California’s recorded history began when, in 1542, Juan Rodríguez Cabrillo stepped ashore at Point Loma (see page 12). Today, San Diego is America’s seventh-largest city, home to a major naval base, and has been voted one of America’s most desirable cities in which to live. The climate is perfect, the beaches are beautiful, the revitalized downtown area is lively, and the number and range of activities for people of all ages is impressive.
141:One of the best ways to appreciate San Diego’s sparkling beauty is from the sea. You can take a cruise along the bay — boat trips leave from Harbor Drive, just south of the Maritime Museum — out past the man-made Harbor and Shelter Islands and around the tip of the Coronado peninsula (occupied by a US Naval Air Station — the film Top Gun was set nearby in northern San Diego) to Point Loma out on the Pacific coast. The seemingly endless procession of fishing boats, yachts, and US Navy vessels makes for a fascinating tour.
142:The superb 1,200-acre (462-hectare) Balboa Park is situated northeast of Horton Plaza just up 6th Avenue. There are over a half-dozen museums concentrated around El Prado (the Promenade), including the San Diego Museum of Art, the Museum of Man, the Natural History Museum, the Aerospace Historical Center, the Automotive Museum, and the Reuben H. Fleet Space Theater and Science Center. San Diego’s renowned Old Globe Theatre is one of five stages in the area, offering entertainment from Shakespeare to favorite American musicals.
143:The highlight of the park is the San Diego Zoo, one of the finest in the world. Established in 1922, the zoo was a pioneer in the use of moats, ravines, rocks, and embankments rather than bars and cages, giving the animals as large, free, and natural a living space as possible. It is famous for its Sumatran tigers and Malaysian sun bears as well as a colony of koala bears — the only breeding population outside Australia. You can enjoy a bird’s-eye view of the zoo from the Skyfari aerial tramway, or take a guided tour bus. An extension of the zoo is located 30 miles (48 km) north at the San Diego Wild Animal Park in Escondido, where 2,500 animals, including zebra, lions, elephants, cheetahs, and rhinoceros, roam freely.
144:The oldest part of San Diego is situated 3 miles (4.8 km) north of downtown in the area known as Old Town (bounded by Juan, Congress, Twiggs, and Wallace streets). Here, in 1769, the European colonization of California commenced, beginning with the construction of Father Junípero Serra’s Mission San Diego de Alcala. In this area of restored adobe buildings, you can enjoy a rest under the palms and eucalyptus of Plaza Vieja (originally the town plaza and bullfight arena before the Yankees arrived), browse among the stalls selling Mexican handicrafts, or eat at one of the many restaurants.
145:Cabrillo National Monument, situated on the Point Loma promontory (I-5/I-8 exit on Rosecrans Street and follow the signs), celebrates the man who discovered San Diego Bay. You can walk the trails around the point, visit the Old Point Loma Lighthouse, and at low tide explore the tide pools for crabs, starfish, anemone, and, if you are lucky, perhaps even the odd, elusive octopus. If you’re here between December and March, watch for migrating gray whales from the look-out point near the lighthouse.
147:San Diego’s beaches are truly beautiful and remarkably unspoiled, stretching for some 27 miles (43 km) up to the elegant suburb of La Jolla (pronounced “la HOY-a,” Spanish for “jewel”), whose centerpiece is the tiny rock basin of La Jolla Cove. The rocky coast to the south is marvelous for walking, and away from the ocean there are stylish shops and elegant restaurants to visit. The marine life of southern California is splendidly displayed in the Birch Aquarium at Scripps, which is spectacularly sited on the hilltop above La Jolla.`

Explanation:
This is similar to the -c option, where it searches for a specific string. However, -n does so inside a textfile, and actually lists the number line. It looked for lines that contained "San Diego" inside the California-WhatToDo.txt file. This was useful for filtering out cities that weren't San Diego, and giving the line number. This is useful for going back into the text file to find extra information from the line numbers that the -c option didn't provide.

**EXAMPLE 2)**

Input:
`andyho@Andys-MacBook-Air berlitz2 % grep -n "Los Angeles" California-WhereToGo.txt `
Output:
`6:Many Californians would like to divide their state into two new states, Northern and Southern California — corresponding to what they believe to be two distinct frames of mind as represented by San Francisco and Los Angeles. In fact you will find a little bit of both — San Francisco’s sophistication and Los Angeles’ sunny craziness — all over the place.
7:Our journey begins with San Francisco and its nearby attractions and works its way down the coast to Los Angeles and San Diego before heading inland to the mountains and deserts of the Sierra Nevada and Death Valley. You can turn this itinerary upside down if you prefer, but either way, you should also consider making an excursion to Las Vegas, California’s favorite out-of-state playground.
8:You can get to almost all these places by train or bus, and air travel is quite cheap. However, the car is king, and it’s difficult to enjoy the full scope of this vast and varied landscape without driving. San Francisco is unusual for California in that it is a walker’s town, with buses and cable cars to help you up and down the hills. Los Angeles is undeniably car country, though it is trying to alleviate its congestion and pollution by building a light-rail network. Out-of-town attractions such as the national parks, and especially Death Valley, are most easily reached by car, although once there it’s more rewarding to leave your vehicle behind and explore on foot.
81:Beyond San Simeon the rugged coastline begins to relent, and farms and oil rigs take the place of crags and canyons. Rural Route 1 joins the multi-lane US Highway 101 at San Luis Obispo for the final leg to Los Angeles, but two places are worth a detour from the freeway.
83:When you get to Santa Barbara you know for sure that you’ve arrived in Southern California. Its palm-fringed streets, red-tile pavements, and low-rise Spanish Revival buildings spread up the hillsides from the beautiful beach, oozing sun-tanned health and the scent of money. It’s a favorite weekend retreat for many of Los Angeles’ wealthier residents.
85:Los Angeles
86:Los Angeles is the quintessential 20th-century city. Only modern technology could have turned this former patch of desert into one of the world’s most flourishing metropolises.
90:L.A.’s downtown commercial district is steadily becoming a more attractive and culturally active area, but the activity here diminishes once the workday is over. Surrounded by three freeways and the river, historically this district is the heart of Los Angeles. It’s now also the terminus of L.A.’s new Metro Rail system, which is housed in the Spanish Mission–style Union Station.
91:El Pueblo de Los Angeles State Historic Park preserves a few blocks of the original Mexican village around which the city grew up. The center is Olvera Street, a bustling Mexican marketplace lined with colorful handicraft and food stalls and historic buildings, including the Avila Adobe, L.A.’s first house, dating from 1818. Half of California’s Mexican-American (chicano) population lives in central Los Angeles, but you’ll find the full range of the city’s ethnic population — represented by comestibles — at Grand Central Market, north of Pershing Square.
96:If you’re heading west from downtown, avoid the freeway and follow another great thoroughfare, Wilshire Boulevard. Once an Indian trail, in its heyday this 16-mile (25-km) roadway glittered with the prosperity of its department stores and luxury hotels. A living museum of the Art Deco architecture that characterized Los Angeles’s rise to greatness during the 1920s and 1930s, the section of Wilshire between La Brea and Fairfax avenues, known as the “miracle mile,” is slowly being renovated after years of neglect. Notable buildings include the former Bullocks Wilshire department store standing at the corner of Kingsley, and the Franklin Life Insurance building situated at Van Ness and Wilshire.
98:Next door to the tar pits is the Los Angeles County Museum of Art (LACMA), whose provocative modern architecture houses one of the state’s best art collections, including outstanding examples of Nepalese, Indian, and Tibetan art, Japanese scroll paintings, pre-Columbian art, and German Expressionist drawings. Other highlights include important works by Rembrandt, Dürer, Frans Hals, Picasso, and the Impressionists.
104:A couple of freeway exits away is the Hollywood Bowl, a splendid open-air amphitheater where the Los Angeles Philharmonic Orchestra holds concerts under the gigantic illuminated letters of the Hollywood sign planted up in the hills.
106:While you’re on the north side of town, take a drive around the Hollywood Hills for a superb view of the city. The classic Los Angeles cruise is along Mulholland Drive. On a clear day you can see Long Beach, 25-miles (40-km) away across the vast, sprawling metropolis.
112:There’s a more scholarly feel to Los Angeles around the campus of UCLA (University of California-Los Angeles) at Westwood Village. The Village is a fine place in which to see a movie — new films always open here first. At the edge of Westwood, the UCLA/Armand Hammer Museum of Art and Cultural Center (10899 Wilshire Boulevard) features a fabulous collection of paintings personally collected over the last fifty years by Hammer. If your visit to Hollywood has filled you with nostalgia for the great days of cinema, then you might like to pay homage to Marilyn Monroe in Westwood Memorial Park (1212 Glendon Avenue, south of Wilshire Boulevard), where a modest plaque bears silent testimony to the actress.
115:“The beach,” as locals refer to it, stretches some 72 miles (115 km) from Malibu, through Santa Monica, Venice, Marina del Rey, Hermosa, and Redondo to Palos Verdes, before the white sands run into the pollution around the San Pedro and Long Beach shipyards. There’s no better way to get the special feel of Los Angeles than by heading right down to the beach, because in L.A. the beach is not just for holidays and weekends — it’s a year-round playground, community center, gymnasium, solarium, and singles bar.
121:South of the more staid Marina del Rey, the world’s largest small-boat harbor, the beaches continue in an unbroken golden curve — Dockweiler, Manhattan, Hermosa, Redondo — to the rocky bluffs of Palos Verdes. Around the point lies San Pedro, the Port of Los Angeles, and the city of Long Beach.
124:The great mass of Los Angeles’s population lives in the sprawling suburbs of the valleys — the San Fernando Valley north of the Hollywood Hills and the San Gabriel Valley stretching east towards San Bernardino. It’s composed mainly of suburbs and uninspired strip centers (block-long low-rise shopping malls), but there are a few reasons to drop by.`

Explanation:
In this example, I searched for lines that contained Los Angeles inside California-WhatToDo.txt. This is useful for a Los Angeles native that thinks that their city revolves around the world and doesn't want to do research on other cities. They get an idea where information about Los Angeles ends because this command actually lists the line number, although this might not be entirely accurate because there may be information about LA that doesn't have "Los Angeles" in the line, but we still have a general idea.


