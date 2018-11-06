# appsquatting
Abstract:  Domain squatting, a well-known adversarial tactic that attackersregister domain names that are purposefully similar to popular do-mains, had been observed and studied for decades. Recent studiessuggested that squatting-like attacks have been penetrated to vari-ous problem spaces. In this work, we demonstrates that squattingbehaviors are also prevalent in the mobile app ecosystem with adifferent manner, which we called “App Squatting”. Specifically,attackers may release app with identifiers (e.g., app name, pack-age name or developer name) that are confusingly similar to thosebelonging to popular apps or large Internet brands. This paperpresents the first in-depth measurement study of app squatting.We first summarize 11 deformation models for app squatting byinvestigating squatting apps being collected. In particular, we pro-pose and implement a tool named “AppCrazy”, which is capable ofautomatically generating variations of app identifiers, to facilitateour analyses. We have applied AppCrazy to the top-500 popularapps in Google Play, obtained 224,322 deformation keywords, andeventually collected 13,738 squatting apps accordingly. Further in-vestigation suggests that more than 51% of those squatting apps aremalicious. Our study demonstrates the urge to identify and preventapp squatting abuse. We have released all the identified squattingapps to the research community, and we will further release Ap-pCrazy and provide easy-to-use web service in the future


Squatting-generation Models:
1、Mutation-based Models. This kind of models generate squatting
names based on either typographical errors or abusing the
pronunciation similarity of different words. We have manually
summarized 9 mutation-based models as follows.
    (1) Case Substitution: Replace an uppercase character with a
lowercase one (or vice versa), e.g., “Facebook” into “facebook”.
Note that the package names in most app markets
(e.g., Google Play) are case sensitive.
    (2) Vowel Character Insertion: Insert another vowel character
after a vowel character, e.g., “Facebook” into “Faceebook”.
    (3) Vowel Character Deletion: Delete one or more vowel characters,
e.g., “Facebook” into “Facbook”.
    (4) Vowel Character Substitution: Replace a vowel characters with
other four vowel characters, e.g., “Facebook” into “Fecebook”.
    (5) Double Character Insertion: Insert a same character between
two consecutive identical characters, e.g., “Facebook” into
“Faceboook”.
    (6) Double Character Deletion: Delete one or two characters who
are the consecutive identical characters, e.g., “Facebook” into
“Facebok”, and “Facebook” into “Facebk”.
    (7) Punctuation Substitution: Replace punctuation with other
ones ( including space, underscore and dot), e.g.,
“com.facebook.katana” into “com.facebook_katana”.
    (8) Punctuation Deletion: Delete a punctuation (including space,
underscore and dot), e.g., “com.facebook.katana” into
“com.facebookkatana”.
    (9) Common Misspelling Mistakes Substitution: Replace specific
characters with 9 common misspelling mistakes[57]. e.g.,
“Facebook” into “Faceb00k”.
2、Combosquatting Generation Models. we refer it as
the attempt of “borrowing” a popular app’s reputation characteristics
by integrating a popular app’s name or package name with
other characters or words. For example, “Angry Birds 2”, or “Angry
Birds Update”. App Combosquatting differs from other forms of
app squatting in two fundamental ways: combosquatting does
not involve the spelling deviation from the original app identifier
names; it requires the original app identifier names to be intact
within a set of other characters. As a result, we define two kinds of
Combosquatting generation models.
    (1) String Expansion: Insert characters before or after the identifier
name, e.g., “Facebook” into “Facebook1”.
    (2) String Rearrangement: Split the string into elements based
on character dot, and rearrangement the elements, e.g.,
“com.facebook.katana” into “com.katana.facebook”,
