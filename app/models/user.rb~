class User
  include Mongoid::Document
  HOBBIES = ["Playing cricket", "Playing chess", "Reading Books", "Watching TV", "Singing Songs"]

  field :name, type: String
  field :birthdate, type: Date
  field :gender, type: String
  field :address, type: String
  field :country, type: String
  field :pin_code, type: Integer
  field :email, type: String
  field :mobile_number, type: String
  field :hobbies, type: Array

  validates :name, :birthdate, :address, :country, :pin_code, :email, :mobile_number, presence: true
#  validates :email, :format => { with: /^[-a-z0-9_+\.]+\@([-a-z0-9]+\.)+[a-z0-9]{2,4}$/i, message: "Not a valid email address"}
  validates :email, uniqueness: true
  validates :pin_code, length: {is: 6}
  validates :pin_code, numericality: {only_integer: true}
  validates :mobile_number, :format => { with: /(^\s*$|^\s*[789]\d{9}\s*$)/, :message => "Please provide 10 digit mobile number." }
end
