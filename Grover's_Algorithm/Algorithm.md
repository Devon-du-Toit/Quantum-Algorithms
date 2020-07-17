
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

__The Algorithm__


</br>

__The Quantum Circuit__

