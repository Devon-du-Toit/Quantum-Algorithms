
<h1> Grover's Algorithm </h1>

</br></br>

<h2>Problem</h2>
  
Consider a large list of __*N*__ items. Within the list is a single element (__*w*__) that we wish to locate. 

</br></br>

<h2>Classical Solution</h2>

We could find the element by going one-by-one through each element within the list. We would need to search through __*N/2*__ elements on average to locate our specific element. In the worst case we would need to do __*N*__ searches.

</br></br>

<h2>Quantum Solution</h2>

On a Quantum Computer we can find the element within __&#8730; &#x305;N&#x305;__ searches by employing Grover's amplitude aplification technique.
</br>

__Method__

We need to convert the list into a function __*f*__ which returns __*f(x) = 0*__ for all elements excluding the required element __*w*__, which will return __*f(w) = 1*__. For the quantum algorithm, we supply the function all elements in superposition and encode the function into a unitary matrix (now the oracle).

First we choose a binary encoding of elements __*x, w ∈ {0, 1}<sup>n</sup>*__ such that __*N = 2<sup>n</sup>*__. Next we define the oracle (__*U<sub>f</sub>*__) to act upon the basis states __*|x>*__ by __*U<sub>f</sub> |x> = (-1)<sup>f(x)</sup>|x>*__.

As __*x*__ is not the required element, the oracle leaves the state unaffected. For __*|w>*__, however, the oracle maps __*U<sub>f</sub> = -|w>*__. This correponds to a origin reflection for the market element in __*N = 2<sup>n</sup>*__ dimensional vector space.

</br>

__Amplitude Amplification__

The algorithm amplifies the required element and shrinks the other elements's amplitudes. This is done by reflections upon an 2-dimensional vector space __*C<sup>n</sup*__. The two states we consider is the required element __*|w>*__ and and the uniform superposition __*|s>*__ defined by:</br>
![superposition](https://user-images.githubusercontent.com/68278907/87779800-b856c800-c82d-11ea-8795-85eb2e5b7e24.jpg)

These two states are not perpendiculat, as __*|w>*__ occurs in superposition with amplitude __*N<sup>-1/2</sup>*__ as well. We therefore introduce another state __*|s'>*__ within span of the two vectors, perpendicular to __*|w>*__. This is obtained by removing __*|w>*__ from __*|s>*__ and rescaling.

1. We construct __*|s> = H<sup>⊗n</sup>|0><sup>n</sup>*__:

![sk1](https://user-images.githubusercontent.com/68278907/87781143-65324480-c830-11ea-965f-6f99d73d4d5e.jpg)

![sk2](https://user-images.githubusercontent.com/68278907/87789926-142a4c80-c840-11ea-933e-7431cc856807.jpg)




</br>

__The Quantum Circuit__

