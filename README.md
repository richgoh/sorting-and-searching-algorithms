# sorting-and-searching-algorithms


Implementation of Insertion Sort using JavaScript
function triInsertion(arr) {
    // Parcourir le tableau en commençant par le deuxième élément
    for (let i = 1; i < arr.length; i++) {
        // Stocker l'élément actuel à insérer
        let courant = arr[i];
        // Commencer la comparaison avec les éléments avant lui
        let j = i - 1;
        
        // Déplacer les éléments de arr[0..i-1], qui sont plus grands que courant,
        // vers une position devant leur position actuelle
        while (j >= 0 && arr[j] > courant) {
            arr[j + 1] = arr[j];
            j--;
        }
        
        // Insérer l'élément courant à sa position correcte
        arr[j + 1] = courant;
    }
    return arr;
}

// Exemple d'utilisation :
const tableau = [12, 11, 13, 5, 6];
console.log("Tableau original :", tableau);
console.log("Tableau trié :", triInsertion(tableau));
