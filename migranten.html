<?php
// FKFA Kontaktformular - PHP Mailer
// Empfänger-E-Mail hier eintragen:
$empfaenger = "kontakt@freundeskreis-fluechtlinge.de";

// Nur POST-Anfragen verarbeiten
if ($_SERVER['REQUEST_METHOD'] !== 'POST') {
    header('Location: kontakt.html');
    exit;
}

// Eingaben bereinigen
function clean($str) {
    return htmlspecialchars(strip_tags(trim($str)), ENT_QUOTES, 'UTF-8');
}

$name     = clean($_POST['name'] ?? '');
$email    = clean($_POST['email'] ?? '');
$thema    = clean($_POST['thema'] ?? '');
$nachricht = clean($_POST['nachricht'] ?? '');

// Validierung
$fehler = [];
if (empty($name))                          $fehler[] = "Bitte gib deinen Namen ein.";
if (empty($email) || !filter_var($_POST['email'], FILTER_VALIDATE_EMAIL))
                                           $fehler[] = "Bitte gib eine gültige E-Mail-Adresse ein.";
if (empty($nachricht))                     $fehler[] = "Bitte gib eine Nachricht ein.";

if (!empty($fehler)) {
    // Zurück zum Formular mit Fehlermeldung
    $fehlerText = urlencode(implode("|", $fehler));
    header("Location: kontakt.html?fehler=$fehlerText");
    exit;
}

// E-Mail zusammenstellen
$betreff = "Kontaktanfrage via Website: $thema";
$text    = "Neue Nachricht über das Kontaktformular auf freundeskreis-fluechtlinge.de\n";
$text   .= "=================================================================\n\n";
$text   .= "Name:    $name\n";
$text   .= "E-Mail:  $email\n";
$text   .= "Thema:   $thema\n\n";
$text   .= "Nachricht:\n$nachricht\n\n";
$text   .= "=================================================================\n";
$text   .= "Gesendet am: " . date('d.m.Y H:i') . " Uhr\n";

$headers  = "From: website@freundeskreis-fluechtlinge.de\r\n";
$headers .= "Reply-To: $email\r\n";
$headers .= "Content-Type: text/plain; charset=UTF-8\r\n";

// Senden
$gesendet = mail($empfaenger, $betreff, $text, $headers);

if ($gesendet) {
    header("Location: kontakt.html?erfolg=1");
} else {
    header("Location: kontakt.html?fehler=" . urlencode("Die E-Mail konnte leider nicht gesendet werden. Bitte ruft uns direkt an."));
}
exit;
?>
