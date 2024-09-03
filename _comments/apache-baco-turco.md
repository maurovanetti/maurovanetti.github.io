---
title: Anche Apache ha dovuto combattere il baco turco…
post: baco-turco
date: 2010-07-30 15:39:00 +0200
author: Mauro Vanetti
---
    /**
     Convert the string passed as argument to a level. If the
     conversion fails, then this method returns the value of
     `defaultLevel`.
    */
    public static Level toLevel(String sArg, Level defaultLevel) {
    if(sArg == null)
       return defaultLevel;

    String s = sArg.toUpperCase();

    if(s.equals("ALL")) return Level.ALL;
    if(s.equals("DEBUG")) return Level.DEBUG;
    if(s.equals("INFO"))  return Level.INFO;
    if(s.equals("WARN"))  return Level.WARN;
    if(s.equals("ERROR")) return Level.ERROR;
    if(s.equals("FATAL")) return Level.FATAL;
    if(s.equals("OFF")) return Level.OFF;
    if(s.equals("TRACE")) return Level.TRACE;
    //
    //   For Turkish i problem, see bug 40937
    //
    if(s.equals("\u0130NFO")) return Level.INFO;
    return defaultLevel;
    }

(Dal sorgente di [org.apache.log4j.Level](https://web.archive.org/web/20120315181202/http://www.docjar.com/html/api/org/apache/log4j/Level.java.html))