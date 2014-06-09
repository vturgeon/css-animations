Animations créées dans le cadre du cours de technique d'animations

Read me

Liste des animations :

rebond

arrivee_depart

file_rotate

pulse_shadow

rotate_disparition

Guide d’installation :

Pour utiliser les animations dans votre site web, simplement « dropper » la feuille de style (style.css) dans la section head de votre fichier HTML. Ajouter ensuite la classe animation à un élément suivi de la classe portant le nom de l’animation voulue (par exemple class = "animation rebond".

Changer le temps et le délai :

La classe animation a par défaut un temps d’animation de 1 seconde et un délai de 0 secondes (l’animation démarre automatiquement lorsque la page web est téléchargée). Pour changer le temps d’animation ainsi que le délai des animations, ouvrez la feuille de style.css. Repérez la classe .animation et changez à l’intérieur de celle-ci la durée de l’animation (par exemple animation-duration : 3s;). Pour changer le délai avant que l’animation démarre, toujours dans la classe .animation, changez le délai d’animation (par exemple animation-delay : 2s;).

Objet animé à l’infini :

Il est possible de faire durer l’animation sur votre objet à l’infini. Pour ce faire, vous devez installer la classe infinite sur l’élément de votre choix (par exemple class = "animation rebond infinite".

Direction de l’animation :

Pour faire alterner l’animation (l’animation s’exécute et revient dans le sens inverse), ajouter la classe alternate sur l’objet de votre choix (par exemple class = "animation file_rotate infinite alternate".

Propriétés spécifiques à changer sur quelques animations :

rebond

Lorsque l’élément rebondit, celui-ci change de couleur et revient ensuite à sa couleur initiale lorsque le rebond est terminé. Pour changer la couleur lors du rebond, allez dans la feuille de style (style.css) et changer le background-color à la couleur de votre choix. **Ne pas oublier de faire aussi les changements dans les keyframes avec préfixes.

@keyframes rebond

{
	
	0% {
		transform:translateY(0px) scale(1.1, 0.8) ;	
	}
	
	50% {
		transform:translateY(-200px) scale(0.8, 1.1);
		background-color:#F00;	
	}
	
	100% {
		transform:translateY(0px) scale(1.1, 0.8) ;	
	}

}

file_rotate

Pour faire tourner l’élément dans le sens contraire des aiguilles d’une montre, allez dans la feuille de style (style.css) et changer la propriété rotate au keyframe 100% en valeur négative (par exemple : transform:translate(300px, -100px) rotate(-180deg) scale(1.5, 1.5);. **Ne pas oublier de faire aussi les changements dans les keyframes avec préfixes.

@keyframes file_rotate

{
	
	0% {
		transform:translate(0px, 0px) rotate(0deg);	
	}
	
	30% {
		transform:translate(300px, -100px) rotate(0deg) scale(1, 1);
	}
	
	100% {
		transform:translate(300px, -100px) rotate(180deg) scale(1.5, 1.5);	
	}

}

pulse_shadow

Pour changer la couleur de l’ombre, allez dans la feuille de style (style.css) et changez le box-shadow à la couleur de votre choix. Pour changer la couleur du pulse, changez le background-color à la couleur de votre choix. **Ne pas oublier de faire aussi les changements dans les keyframes avec préfixes.
@keyframes pulse_shadow

{
	
	0, 100% {
		transform:scale(1,1);
		box-shadow: 0px 0px 0px #000;
	
	50% {
		transform:scale(1.1,1.1);
		box-shadow: 0px 0px 15px #000;
		background-color:#00C;
	}

}

rotate_disparition

Pour faire tourner l’élément dans le sens contraire des aiguilles d’une montre, allez dans la feuille de style (style.css) et changer la propriété rotate au keyframe 33.3%, 66.6% et 100%  en valeur négative (par exemple : transform:rotate(-360deg) scale(1, 1); ).

@keyframes rotate_disparition

{
	
	0% {
		transform:rotate(0deg) scale(0, 0);
		opacity:1;
	}
	
	33.3% {
		transform:rotate(360deg) scale(1, 1);
		opacity:1;
	}
	
	66.6%{
		transform:rotate(360deg) scale(1, 1);
		opacity:1;
	}
	
	100%{
		transform:rotate(360deg) scale(1, 1);
		opacity:0;
	}

}
