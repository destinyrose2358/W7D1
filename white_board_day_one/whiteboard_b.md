class Array
  def my_reduce(acc = nil, &prc)
    if acc.nil?
      acc = self[0]
      i = 1
    else
      i = 0
    end

    (i...self.length).each do |idx|
      acc = prc.call(acc, self[idx])
    end

    acc
  end
end