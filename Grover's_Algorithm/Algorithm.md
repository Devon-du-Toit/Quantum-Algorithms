
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

Above, a two-dimensional plane spanned by perpendicular vectors __*|w>*__ and __*|s>*__. The initial state is expressed as __*|s>=sinθ(w)+cosθ(s')*__, where __*θ = arcsin<s|w> = arcsin(1/&#8730; &#x305;N&#x305;)*__


![sk2](https://user-images.githubusercontent.com/68278907/87790167-6b302180-c840-11ea-8976-2b024b1d069a.jpg)



Above, a graph of amplitudes of state __*|s>*__ for __*N=2<sup>2</sup>*__

2. Apply the oracle reflection (__*U<sub>f</sub>*__) to __*|s>*__.

![sk3](https://user-images.githubusercontent.com/68278907/87809400-a1c76580-c85b-11ea-92f6-c4cb44d1cca5.jpg)

![sk4](https://user-images.githubusercontent.com/68278907/87810063-ab9d9880-c85c-11ea-863f-7f883ad5bc5f.jpg)

This implies a reflection of __*|s>*__ around __*|s'>*__ and amplitude __*|w>*__ becomes negative, thus the average amplitude has been lowered.

3. Additional reflection __*U<sub>s</sub>*__ is now reflected about __*|s>*__: __*U<sub>s</sub>=2|s><s|-1*__. This maps the state to __*U<sub>s</sub>U<sub>f</sub>|s>*__ and completes the transformation. 

![sk5](https://user-images.githubusercontent.com/68278907/87810934-169b9f00-c85e-11ea-82ea-b75d4bbd80ac.jpg)

![sk6](https://user-images.githubusercontent.com/68278907/87811251-a3465d00-c85e-11ea-8d9b-748891157021.jpg)


The transformation __*U<sub>s</sub>U<sub>f</sub>|s>*__ rotates states __*|s>*__ towards __*|w>*__. Considering the bar diagram, reflection __*U<sub>s</sub>*__ isa reflection about the average amplitude. As the average amplitude is lowered by the first reflection, this transformation amplifies the negative amplitude of __*|w>*__, while it decreases the other amplitudes. Step 2 is again applied to repeat the application until __*|w>*__ is found.

If __*t*__ is the number of steps, we will be in state __*|ψt>*__ where __*|ψt>=(U<sub>s</sub>U<sub>f</sub>)<sup>t</sup>|s>*__.

The average number of steps required is roughly __*&#8730; &#x305;N&#x305;*__.

