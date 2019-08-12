an object is an instance of a class, which comes from the Object class

a ||= b is shorthand for a = a || b which is a way to reassign a only if it wasn't already assigned

unit testing is testing the methods for specific behavior


design a parking lot using oop

parking lot should have floors

spaces should account for vehicle size, compact, regular

motorcycle can take spots anywhere
car can take regular spot
busses take multiple spaces

```rb

class ParkingLot

def initialize(floors)
    @floors = floors
end

def add_vehicle(vehicle)
    #searches through the floors for a valid space
end

def remove_vehicle(vehicle)
    #searches through floors and removes the specified vehicle
end

end

class Floor

    def initialize(strips)
        @strips = strips
    end

    def place_vehicle

    def remove_vehicle

end

class Strip

def initialize(spaces)
    @spaces = spaces
end

def place_vehicle(vehicle)
    #search through its spaces and place the vehicle if it can
end

def remove_vehicle(vehicle)
end

end

class Compact < Space

    def initialize(car = nil)
        super(car, 1)
    end

end

class Regular < Space

    def initialize(car = nil)
        super(car, 2)
    end

end

class Space

    def initialize(car = nil, size = 0)
        @car = car
        @size = size
    end

    def empty?
        car.nil?
    end

    def vehicle_fits?(vehicle)

    end

    def add_car

    def remove car
end

class Vehicle
    attr_reader :size

    def initialize(size = 0)
        @size = size
    end
end

class Motorcycle

```


dfs assume there is a node class

takes in a value on initialize

starting at root, node it takes a target or proc


```rb


class Node


    def dfs(target = nil, &prc)
        raise "Need a proc or target" if target.nil? && prc.nil?
        prc ||= Proc.new { |node| target == node.value }

        return self if prc.call(self)

        self.children.each do |child|
            result = child.dfs(&prc)
            return result unless result.nil?
        end
        nil
    end


end


```
