---
layout: default
title: Anmeldung
---

# Dein erster Besuch beim CoderDojo Luzern

So läuft dein erster Besuch beim CoderDojo Luzern ab:

1. Lies die Informationen durch, die wir für dich zusammengestellt haben.<br/>
   <a class="btn btn-material-luzern-blue" href="/infos/kinder.html" target="_blank">Infos für Coder&nbsp;...</a>&nbsp;

1. Lies gemeinsam mit deinen Eltern die Informationen durch, die wir für sie zusammengestellt haben.<br/>
   <a class="btn btn-material-luzern-blue" href="/infos/kinder.html" target="_blank">Infos für Eltern&nbsp;...</a>&nbsp;

1. Du füllst das <a href="#form">Anmeldeformular</a> unten aus.<br/>
   <a class="btn btn-material-luzern-blue" href="#form">Anmeldung&nbsp;...</a>&nbsp;

1. Wir schicken dir eine Email und bestätigen den Termin.<br/>
_Bitte beachte, dass es aus organisatorischen Gründen eine Weile dauern kann, bis du von uns eine Email bekommst. Wir geben uns aber Mühe, dass du spätestens in der Woche vor dem CoderDojo Termin diese bekommst. Sollte das nicht der Fall sein, darfst du ohne Weiters trotzdem einfach kommen._

1. Du kommst mit <a href="/infos/eltern.html#Laptop" target="_blank">deinem Laptop</a> zum CoderDojo Luzern in die <a href="#bbv">bbv</a>. Falls du keinen eigenen Laptop hast, gib im Anmeldeformular an, dass du ein Leihgerät brauchst.

1. Eine Mentorin oder ein Mentor vom CoderDojo Luzern zeigt dir, wie das CoderDojo funktioniert und gibt dir Tipps, womit und wie du starten könntest.

## <a name="form" />Anmeldung

<div class="row registration-form">
  <div class="col-sm-10 col-md-8 col-lg-6">
    <div class="card card-block">
        <div class="registration-finished hide">
            <h3>Anmeldung abgeschlossen</h3>
            <p>Danke für deine Anmeldung, wir freuen uns schon auf dich!</p>
        </div>
        <div class="registration-error hide">
            <h3>Fehler bei der Anmeldung</h3>
            <p>Die Anmeldung ist leider fehlgeschlagen. Bitte kontaktiere uns unter <a href="mailto:coderdojo.luzern@gmail.com">coderdojo.luzern@gmail.com</a>.</p>
        </div>
        <form class="registration" id="registration-form" method="POST" action="https://formspree.io/coderdojo.luzern@gmail.com">
            <h3>Ich möchte zum ersten Mal zum CoderDojo kommen</h3>
            <div class="form-group">
              <label for="event">Termin</label>
              <select name="Termin" id="event" class="form-control" required="required">
              </select>
              <div style="padding-top: 15px"><small><small>Der Ort kann sich in seltenen Fällen ändern. Bitte überprüfe einige Tage vor der Veranstaltung unter <a href="termine.html" target="_blank">Termine</a>, ob der Veranstaltungsort geändert wurde.</small></small></div>
            </div>
            <div class="form-group">
                <label for="givenName">Vorname</label>
                <input name="Vorname" type="text" class="form-control" id="givenName" required="required"
                    oninvalid="this.setCustomValidity('Gib bitte den Vornamen des Teilnehmers an.')" oninput="setCustomValidity('')">
            </div>
            <div class="form-group">
                <label for="familyName">Nachname</label>
                <input name="Nachname" type="text" class="form-control" id="familyName" required="required"
                    oninvalid="this.setCustomValidity('Gib bitte den Nachnamen des Teilnehmers an.')" oninput="setCustomValidity('')">
            </div>
            <div class="form-group">
                <label for="gender">Mädchen / Junge</label>
                <select name="Geschlecht" id="gender" class="form-control" required="required"
                    oninvalid="this.setCustomValidity('Gib bitte an, ob der Teilnehmer ein Mädchen oder ein Junge ist.')" oninput="setCustomValidity('')">
                    <option value="" disabled selected></option>
                    <option value="f">Mädchen</option>
                    <option value="m">Junge</option>
                </select>
            </div>
            <div class="form-group">
                <label for="yearOfBirth">Geburtsjahr</label>
                <select name="Geburtsjahr" id="yearOfBirth" class="form-control" required="required"
                    oninvalid="this.setCustomValidity('Gib bitte das Geburtsjahr des Teilnehmers an.')" oninput="setCustomValidity('')">
                    <option value="" disabled selected></option>
                </select>
            </div>
            <div class="form-group">
                <label for="rentalNotebook">Ich brauche ein Leih-Notebook</label>
                <select name="Braucht ein Notebook" id="rentalNotebook" class="form-control" required="required"
                    oninvalid="this.setCustomValidity('Gib bitte an, ober der Teilnehmer ein Leih-Notebook braucht.')" oninput="setCustomValidity('')">
                    <option value=""></option>
                    <option value="no">Nein</option>
                    <option value="yes">Ja</option>
                </select>
            </div>
            <div class="form-group">
                <label for="email">Email Adresse</label>
                <input name="Email" type="email" class="form-control" id="email" required="required"
                    oninvalid="this.setCustomValidity('Gib uns bitte eine Email-Adresse, unter dir wir dich bei Fragen oder Termin-Änderungen erreichen können.')" oninput="setCustomValidity('')">
            </div>
            <input type="hidden" name="_next" value="/anmeldung-erfolgreich" />
            <input type="hidden" name="_language" value="de" />
            <div class="pull-right">
                <button type="submit" class="btn btn-material-luzern-blue">Anmelden</button>
            </div>
        </form>
    </div>
  </div>
</div>


## <a name="bbv" />Ort

Das CoderDojo findet üblicherweise in der [bbv Software Services AG](https://www.bbv.ch){:target="_blank"} im [Blumenrain 10, 6002 Luzern](https://www.google.com/maps/place/bbv+Software+Services+AG/@47.0638419,8.3090783,17z/data=!3m1!4b1!4m5!3m4!1s0x0:0x67769a64439d9bad!8m2!3d47.0638419!4d8.311267){:target="_blank"} statt.
Unter [Termine](termine.html) findest du die aktuellen Termine mit jeweiligem Verstaltungsort.

Der Ort kann sich in seltenen Fällen ändern. Bitte überprüfe einige Tage vor der Veranstaltung unter <a href="termine.html" target="_blank">Termine</a>, ob der Veranstaltungsort geändert wurde.

## bbv Software Services AG

Vielen Dank an die [bbv Software Services AG](https://www.bbv.ch){:target="_blank"} für die grossartigen Räumlichkeiten, die wir zur Verfügung gestellt bekommen!


<script language="javascript">
$.get("https://www.googleapis.com/calendar/v3/calendars/coderdojo.luzern@gmail.com/events?key=AIzaSyDuL2gUksesWq33UDNoACL4mdyjQcsS6vk", function(data) {
    const comp = function(a, b){ new Date(a.start.dateTime || a.start.date).getTime() - new Date(b.start.dateTime || b.start.date).getTime(); };
    data.items.filter(function(item){ return item && item.hasOwnProperty('status') && item.status !== 'cancelled'; }).sort(comp).slice(0, 3).forEach(function(item) {
         $("#event").append("<option value=\"" + item.start.dateTime + "\">" + (new moment(item.start.dateTime)).format("Do MMM YYYY, H:mm") + " Uhr @ " + (item.location ? item.location : "bbv Software Services AG Luzern") + "</option>");
    });

    var currentYear = new moment().year();
    for (var i = currentYear - 6; i >= currentYear - 18; i--) {
        $("#yearOfBirth").append("<option value=\"" + i.toString() + "\">" + i.toString() + "</option>");
    }
});
</script>
