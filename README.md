# displacement
/**
 * Calculates the displacement given initial position, velocity, and time.
 * 
 * @param {number} initialPosition - The initial position in meters.
 * @param {number} velocity - The velocity in meters per second.
 * @param {number} time - The time in seconds.
 * @returns {number} The displacement in meters.
 */
function calculateDisplacement(initialPosition, velocity, time) {
  try {
    // Check if all arguments are numbers
    if (
      typeof initialPosition !== "number" ||
      typeof velocity !== "number" ||
      typeof time !== "number"
    ) {
      throw new TypeError("All arguments must be numbers");
    }

    // Calculate and return the displacement
    return initialPosition + velocity * time;
  } catch (error) {
    // Log the error
    console.error(`Error: ${error}`);
    return 0;
  }
}
