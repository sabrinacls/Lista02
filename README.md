1- Divisible sum pairs
function divisibleSumPairs(n, k, ar) {
  let count = 0;
  for (let i = 0; i < n; i++) {
    for (let j = i + 1; j < n; j++) {
      let sum = ar[i] + ar[j];
      if (sum % k === 0) {
        count++;
      }
    }
  }
  return count;
}

2- cat and mouse
function catAndMouse(x, y, z) {
     let distA = x - z;
    if (distA < 0) distA = -distA;
    let distB = y - z;
    if (distB < 0) distB = -distB;
    if (distA < distB) {
        return "Cat A";
    } else if (distB < distA) {
        return "Cat B";
    } else {
        return "Mouse C";
    }

}

3-jumping on clouds
function jumpingOnClouds(c, k) {
 while (true) {
 let energia = 100;
    let posicao = 0;
    let n = c.length;
    while (true) {
        posicao = (posicao + k) % n;
        energia -= 1;
        if (c[posicao] === 1) {
            energia -= 2;
        }
        if (posicao === 0) {
            break;
        }
    }
    return energia;
}
}

4-repeated strings
function repeatedString(s, n) {
    let countA = 0;
    for (let i = 0; i < s.length; i++) {
        if (s[i] === 'a') {
            countA++;
        }
    }
    let fullRepeats = Math.floor(n / s.length);
    let remainder = n % s.length;
    let countAInRemainder = 0;
    for (let i = 0; i < remainder; i++) {
        if (s[i] === 'a') {
            countAInRemainder++;
        }
    }
    return fullRepeats * countA + countAInRemainder;
}

5- count apples and oranges
function countApplesAndOranges(s, t, a, b, apples, oranges) {
  let appleCount = 0;
    let orangeCount = 0;
    for (let i = 0; i < apples.length; i++) {
        const applePosition = a + apples[i];
        if (applePosition >= s && applePosition <= t) {
            appleCount++;
        }
    }
    for (let i = 0; i < oranges.length; i++) {
        const orangePosition = b + oranges[i];
        if (orangePosition >= s && orangePosition <= t) {
            orangeCount++;
        }
    }
    console.log(appleCount);
    console.log(orangeCount);
}

