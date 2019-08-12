Classesd are blue print/data structures that represent an idea or concept.

Self refers to the object that it currently refers to. This can be at the class or instance level.

Super is a shorthand way of copying methods from the parent class. 


class JukeBox
  def initialize

  end

  def add_songs
    arr.push(new_song)
  end

  def play
    arr.shift
  end

  def take_selection

  end
end

ALBUM 

class User
  def

  end

  def ask_for_album

  end
end

class Node
  def bfs(target, &prc)
    raise "Proc or target not given" if prc.nil? || target.nil?
    prc ||= Proc.new { |node| node.value == target }

    queue = [self]

    while !queue.empty?
      dequeue = queue.shift
      return dequeue if prc.call(dequeue)
      queue += dequeue.children
    end

    nil
  end


end
