Part 1 
1.
/* Initial styles for the button */
.button {
  background-color: #4CAF50;
  color: white;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
  transition: all 0.3s ease; /* Smooth transition for all properties */
}

/* Hover effect */
.button:hover {
  background-color: #45a049;
  transform: scale(1.1); /* Button grows slightly */
}

2. 

@keyframes rotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

/* Apply rotation animation to the spinner */
.spinner {
  width: 50px;
  height: 50px;
  border: 5px solid transparent;
  border-top: 5px solid #3498db;
  border-radius: 50%;
  animation: rotate 1s linear infinite;
}

Part 3
1. 
function calculateArea(length, width) {
  return length * width; // Return the area
}

let area = calculateArea(5, 3); // Call the function with parameters
console.log(area); // Outputs: 15

2.

let globalCount = 0; // Global variable

function incrementCount() {
  let localCount = 5; // Local variable
  globalCount += localCount; // Can access global variable
  console.log("Global count: " + globalCount); // Outputs the global count
  console.log("Local count: " + localCount); // Outputs the local count
}

incrementCount();

3. 
function toggleModal() {
  const modal = document.getElementById("myModal");
  modal.classList.toggle("hidden"); // Toggles the "hidden" class
}
.hidden {
  display: none;
}

.modal {
  /* Initial modal styles, including animations */
  opacity: 0;
  transition: opacity 0.3s ease;
}

.modal.hidden {
  opacity: 0;
}

Part 3
1. 

<button id="openModalBtn" onclick="toggleModal()">Open Modal</button>

<div id="myModal" class="modal hidden">
  <p>Here is a modal!</p>
  <button onclick="toggleModal()">Close</button>
</div>
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.modal {
  display: block;
  animation: fadeIn 0.5s ease-in-out;
}

.hidden {
  display: none;
}

2.

function resetAndTriggerAnimation() {
  const modal = document.getElementById("myModal");
  modal.classList.remove("fadeIn"); // Remove the animation class
  void modal.offsetWidth; // Trigger a reflow to restart the animation
  modal.classList.add("fadeIn"); // Add the animation class again
}

