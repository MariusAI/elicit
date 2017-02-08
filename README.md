# elicit
scraper for elicitatie

This is a collection of scrapers written for the Romanian public tender website. The application is written around the ScraperELicit base-class. You can extend it to create scrapers for different sections of the site.

Here is a list of the different sections of the site, and the classes that handle their scraping
  * Anunturi 
    * Anunturi de intentie                                                   -> ScraperIntentii
    * Anunturi de participare                                                |
    * Anunturi de atribuire                                                  -> ScraperLicitatii
    * Concursuri de solutii                                                  |
    * Concesionari                                                           |
    * Rezultate concursuri de solutii                                        |
    * Anunturi de atribuire concesionari                                     |
    * Consultarea pietei                                                     |
  * Proceduri de atribuire                                                   |
    * Cereri de oferta / Proceduri simplificate                              |
      * Invitatii de participare / Anunturi de participare simplificate      -> ScraperInvitatii
      * Anunturi de atribuire                                                |
    * Cumparari directe                                                      |
      * Cumparari directe in desfasurare                                     |
      * Cumparari directe atribuite                                          |
      * Cumparari directe anulate                                            |
      * Lista notificarilor de atribuire la cumpararea directa               |
    * Licitatii electronice proceduri offline                                |
      * Licitatii electronice in desfasurare                                 |
      * Proceduri offline atribuite                                          |
      * Proceduri offline anulate                                            |
  * Parteneriat PP                                                           |
    * Anunturi de selectie                                                   |
    * Anunturi de atribuire                                                  |

1. REQUIREMENTS:
 Because the website is implemented in ASP, and we need to accurately retrieve the CAPTCHA image, we had to use Selenium / Chromedriver.

 1.1. Selenium Webdriver
  You can install Selenium for Java by following the instructions at http://www.softwaretestingclub.com/profiles/blogs/selenium-2-0-webdriver-how-to-configure-selenium-webdriver-in

 1.2. Chromedriver
  You can install Chromedriver by following the instructions at https://sites.google.com/a/chromium.org/chromedriver/getting-started

 1.3 Tesseract
 Tesseract is needed to automatically solve the CAPTCHA. You can install it by following the instructions at https://github.com/tesseract-ocr/tesseract/wiki
  
  1.4 ImageMagick
  ImageMagick is used to process the CAPTCHA images. You can find a detailed guide on how to install ImageMagick on https://www.imagemagick.org/script/download.php.
  
  1.5 JMagick
  A Java wrapper is needed to use ImageMagick in the application. You can download it from http://www.jmagick.org/. Documentation is available at http://www.jmagick.org/jmagick-doc/. You will have to add the library to the Java search path.

2. COMPILATION
 Create a Java project in your favourite IDE, and export the project as a runnable jar file.

3. RUNNING
 Once you have obtained your elicit.jar file, you can launch it by running 
  
  java -jar elicit.jar [action] [options]

 For detailed help about supported actions and their options, run

  java -jar elicit.jar --help

