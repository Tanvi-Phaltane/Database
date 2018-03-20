# Database
A collection of plants, alongwith their chemical compounds, which are experimentally proven to have anti-diabetic property. 

# Prerequisites
WAMP server v3.1.0 for 64-bit Windows machine(Apache v2.4.27 - PHP v5.6.31 - MySQL v5.7.19)

# Installation 
1) Download server from 'https://sourceforge.net/projects/wampserver/'
1) Install the wamp64 server on your local machine by following the software installation steps.
2) Run wampmanager.exe file
3) Right click on WampServer 'W' logo and select 'Localhost' to check successful running of wamp server
4) Create a new folder 'my_final_proj' in 'wamp64/www' local directory.
5) Place the code files in 'my_final_proj'
6) Again, open localhost and check if 'my_final_proj' folder is visible.
7) Click on 'my_final_proj' folder to view list of files
8) Right click on WampServer 'W' logo and select 'phpMyAdmin'. Login using 'root' as username and no password. 
9) Create a database called 'my_proj_diabetes' and in it table 'final_data_format' with command
CREATE TABLE IF NOT EXISTS `final_data_format` (
  `Plant_name` varchar(10000) NOT NULL,
  `Plant_part` varchar(1000) NOT NULL,
  `Compound_name` varchar(10000) NOT NULL,
  `Diabetes_type` varchar(100) NOT NULL,
  `Effect` varchar(10000) NOT NULL,
  `Experimental_method` varchar(10000) NOT NULL,
  `PubChem_ID` varchar(10000) NOT NULL,
  `Dose` varchar(1000) NOT NULL,
  `Reference` varchar(1000) NOT NULL,
  `Combination_therapy` varchar(10000) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

10) INSERT INTO `final_data_format` (`Plant_name`, `Plant_part`, `Compound_name`, `Diabetes_type`, `Effect`, `Experimental_method`, `PubChem_ID`, `Dose`, `Reference`, `Combination_therapy`) VALUES
('Azadirachta indica', '-', '-', 'Any', 'Significant increase in glucose-6-phosphate dehydrogenase activity and hepatic, skeletal muscle glycogen content after 21 days of treatment given to STZ mice. In immunohistochemical analysis, they observed a regeneration of insulin-producing cells and corresponding increase in the plasma insulin and c-peptide levels with the treatment.', 'STZ induced diabetic mice', '-', '2mg/4ml', 'https://www.hindawi.com/journals/ecam/2011/561625/', 'Not a mixture'),
('Hyphaene thebaica (HT) ', 'fruit (epicarp)', 'vitexin, isovitexin, luteolin 7-O-?-D-glucopyranoside , chrysoeriol 7-O-[6-O-alpha-L-rhamnopyranosyl]-beta-D-glucopyranoside, kaempferol, 4-dimethoxy-3-[6-O-alpha-L-rhamnopyranosyl]-beta-D-glucopyranoside?7, the aglycones, luteolin, chrysoeriol?and kaempferol?,luteolin 7-O-[6-O-alpha-L-rhamnopyranosyl]-beta-D-galactopyranoside?3?and chrysoeriol 7-O-[2-O-beta-D-galactopyranosyl]-alpha-L-arabinofuranoside', 'Any', 'Improved kidney function, reduction in the concentration of both urea and creatinine levels in serums, glutathione peroxidase and superoxide dismutase levels was increased, albumin and total protein levels were reduced', 'Alloxan-diabetic rats', 'vitexin - 5280441,  isovitexin- 162350,  luteolin 7-O-?-D-glucopyranoside -  5280637,  kaempferol - 5280863, luteolin - 5280445,  chrysoeriol - 5280666? ', '-', 'https://www.ncbi.nlm.nih.gov/pubmed/23598921', 'Mixture'),
('Galega officinalis', 'Leaves', 'Galegine', '2', 'Lowering of blood glucose', 'Diabetic mice', '10983', '', 'https://www.ncbi.nlm.nih.gov/pubmed/26132858', 'Not a mixture'),
('Ipomoea batatas (L.) Poir.', '-', 'Anthocyanin', 'Any', 'maltase inhibitory activity', '-', '2-Phenylchromenylium-145858', '0.36 mg/mL', 'https://www.ncbi.nlm.nih.gov/pubmed/11308351', 'Not a mixture'),
('Pharbitis nil (L.) Choisy', '-', 'Anthocyanin', 'Any', 'maltase inhibitory activity', '-', '2-Phenylchromenylium-145858', '0.35 mg/mL', 'https://www.ncbi.nlm.nih.gov/pubmed/11308351', 'Not a mixture'),
('Brassica  oleracea var. Italica', 'Leaves', '-', '2', 'Diabetic   rats   treated   with   the Brassica   oleracea   extracts   regain   body   weight   as compared  to  the  diabetic  control  rats,  which  may  be  due to  its  effect  in  controlling  muscle  wasting.  The  STZ treated  animals  reported a  decrease  in  hepatic  glycogen content  which  may  be  due  to  an  increased  glucose. The elevation of serum insulin in STZ diabetic rats could either  be  due  to  the  insulinotropic  substances  present  in the fractions, which induce the in intact functional beta-cells to produce insulin, or the protection of the functional ?-cells from  further  deterioration  so  that  they  remain  active  and produce insulin.', 'Sprague-Dawley (SD) rats', '-', '800 mg/kg', 'http://impactfactor.org/PDF/IJPPR/8/IJPPR,Vol8,Issue3,Article14.pdf', 'Mixture'),
('Pinus pinaster', 'bark', 'Pycnogenol (catechin, epicatechin, ferulic\nacid, caffeic acid, taxifolin and procyanidins which are oligomeric catechin)', '2', 'Reduced blood glucose levels and improved endothelial function in patients with T2DM. Imhibits alpha-glucosidase activity.', 'Human trials', 'catechin - 9064,procyanidin-107876, epi-catechin - 72276, ferrulic acid- 445858, caffeic acid - 689043, taxifolin - 439533 ', '5.34 mg/mL', 'https://www.ncbi.nlm.nih.gov/pubmed/20378050', 'Mixture'),
('Cinnamomum cassia', 'bark', 'Cinnamon', '1', 'Fasting Blood Glucose level reduction', 'Human trials', '6850775', '1 - 6g daily for 40 - 120days', 'https://www.ncbi.nlm.nih.gov/pubmed/19509199', 'Not a mixture'),
('Camellia sinensis ', 'leaves', '-', 'Any', 'Decreased the serum glucose levels, serum and hepatic malondialdehyde concentration and increased the total antioxidant capacity in diabetic rats (p < 0.05)', 'STZ-diabetic rats', '-', '200mg/kg', 'https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3813194/', 'Mixture'),
('Momordica charantia', 'fruit ', 'Charantin , triterpene, proteid, steroid, alkaloid, inorganic, lipid, and phenolic compounds', 'Any', 'Reduction in fructoseamine levels', 'Human trials', 'Triterpene-15895316', '2000mg/day', 'https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4027280/, https://www.ncbi.nlm.nih.gov/pubmed/21211558/', 'Mixture'),
('Trigonella foenum graecum', 'leaves and seeds', '4-hydroxyisoleucine', '2', 'Increases pancreatic insulin secretion and inhibits sucrose alpha-D-glucosidase and alpha-amylase, lowers cholesterol', 'Human trials', '2773624', '', 'https://www.ncbi.nlm.nih.gov/pubmed/19509199', 'Not a mixture'),
('Gymnema sylvestre', 'leaves', 'Gymnemic acid', 'Any', 'HbA1c level reduction in 2 small trials', 'Human trials', '11953919', '200mg-800mg/day', 'https://www.ncbi.nlm.nih.gov/pubmed/19509199', 'Not a mixture'),
('Phyllanthus Reticulatus', 'leaves', 'Terpenoids glycosides', 'Any', 'Reduction in blood glucose level', 'Alloxan-induced diabetic mice', '-', '1000mg/kg', 'https://www.ncbi.nlm.nih.gov/pubmed/17855019', 'Mixture'),
('Panax Ginseng', 'Fruit, roots', 'Ginsenoside', 'Any', '', 'Diabetic mice', '9898279', '50-150mg/kg', 'https://www.ncbi.nlm.nih.gov/pubmed/12031973', 'Mixture'),
('Zea mays', 'kernel', 'Hirsutrin', 'Any', 'Competitive inhibition of aldose reductase enzyme , reduce osmotic stress in hyperglycemic condition', 'Rats', '5280804', '4.78 microM', 'https://www.hindawi.com/journals/bmri/2013/727143/', 'Not a mixture');
COMMIT;

# Usage for local machine
1) Check browser specified in 'wampmanager.conf' file -> navigator attribute.
    eg: In my case, navigator ="C:/Program Files (x86)/Google/Chrome/Application/chrome.exe"
2) Accordingly open the browser and type localhost/my_final_proj/home.html
3) Similarly, you can load other HTML pages by specifying file name in above URL

A) Basic Search:
    1) In order to qurey the database using basic search (basic_search.html), select any one of the fields (Plant name, Comppund              name, Diabetes type, Experimental evidence, Combination therapy) using drop-down menus
    eg: Plant_name = 'Galega officinalis'
    2) After selecting any one field, click on 'Submit' button.
    3) The user will be directed to 'basic_results.php' page displaying entries related to submitted query.

B) Advanced Search:
    1) User can carry out an advanced search (advanced_search.html) based on Plant name  AND Compound name AND Diabetes type.
    2) The user has to select all fields and then click on Submit.
    3) As the query is AND operated, 'advanced_results.php' page displays entries related to submitted query.

C) Upload Data: 
    1) User needs to fill up the form with details such as Name, Email id, Institute Name and Comments(optional).
    2) User can then upload file in the form of Excel sheet (.xls, .xlsx, .tsv, .csv or .txt accepted)
    3) The file should contain following columns in the same order:
    Plant_name, Plant_part, Compound_name, Diabetes_type, Effect, Experimental_method, PubChem_ID, Dose, Reference, Combination_therapy 
    4) After the user has submitted the data, it will be checked by concerned authorities and then incorporated in the database. A confirmation email will be sent to the submitter on incorporation. 
    






