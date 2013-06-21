# what codeless is

codeless is a slick php framework that focuses on modularity and performance!

# codeless file import criterias and modifiers

	- [file|folder] visible to the development envoirment only

	+ [file|folder] visible to the production envoirment only

	~ [file|folder] files are skipped by the codeless engine

# hierarchy

	\engine (load, db, http [session, cookie, uri, request, response], render [file → html → json → xml → css → less → js → php] )

	\plugin (mysql, locale, auth, google)

		→ plugin [cache → log → tmp → usr, asset, files, tests]

	\module (admin, user, forum, chat, message)

		→ module [cache → log → tmp → usr, asset, files, pages, views, tests]
		
	\public

		→ asset
			→ css (reset.css, style.css, grid.css, typo.css)
			→ js (mootools.js, backbone.js, script.js)
			→ ico (favico.ico)
			→ lang (it.json, en.json, de.json)

		→ cache (log, usr)
		→ pages - virtual folder
		→ views - virtual folder
		→ tests - testing is as important as the content itself