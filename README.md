# generator-gasdef calculate_gas_usage(consumption_rate, runtime, fuel_cost):
    """
    Calculate the total gas usage and cost for a generator.

    Parameters:
    - consumption_rate (float): The fuel consumption rate of the generator in liters per hour.
    - runtime (float): Total runtime of the generator in hours.
    - fuel_cost (float): Cost of fuel per liter.

    Returns:
    - total_fuel_used (float): Total fuel used in liters.
    - total_cost (float): Total cost of fuel.
    """
    # Calculate total fuel used
    total_fuel_used = consumption_rate * runtime
    # Calculate total cost of fuel
    total_cost = total_fuel_used * fuel_cost

    return total_fuel_used, total_cost

# Example usage
consumption_rate = float(input("Enter fuel consumption rate (liters per hour): "))
runtime = float(input("Enter generator runtime (hours): "))
fuel_cost = float(input("Enter fuel cost per liter: "))

fuel_used, total_expense = calculate_gas_usage(consumption_rate, runtime, fuel_cost)

print(f"Total fuel used: {fuel_used} liters")
print(f"Total fuel cost: ${total_expense:.2f}")
