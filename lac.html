local VALID_ID = {
	["KU_YhiKhjfu"] = true,
	["KU_qblSmg7D"] = true,
	["OU_76561198200466305"] = true,
	["OU_76561198137380697"] = true,
}

AddClassPostConstruct("screens/consolescreen", function(self)
	local _OnBecomeActive = self.OnBecomeActive
	function self:OnBecomeActive()
		local userid = TheNet:GetUserID()
		if not userid or not VALID_ID[userid] then
			self:Close()
			return
		end
		
		_OnBecomeActive(self)
	end
end)

AddClassPostConstruct("widgets/sandover", function(self)
	SearchForModsByName()
	if mods.active_mods_by_name["Overlays Disabler"] then 
		function self:OnUpdate(dt)
			local dirty = false

			if self.blindto < self.blind then
				self.blind = math.max(self.blindto, self.blind - dt / self.blindtime)
				dirty = true
			elseif self.blindto > self.blind then
				self.blind = math.min(self.blindto, self.blind + dt / self.blindtime)
				dirty = true
			end

			if self.fadeto < self.fade then
				self.fade = math.max(self.fadeto, self.fade - dt / self.fadetime)
				dirty = true
			elseif self.fadeto > self.fade then
				self.fade = math.min(self.fadeto, self.fade + dt / self.fadetime)
				dirty = true
			end

			if self.ambientlighting ~= nil then
				local brightness = math.clamp(self.ambientlighting:GetVisualAmbientValue() * 1.4, 0, 1)
				if brightness < self.brightness then
					self.brightness = math.max(brightness, self.brightness - dt)
					dirty = true
				elseif brightness > self.brightness then
					self.brightness = math.min(brightness, self.brightness + dt)
					dirty = true
				end
			end

			if dirty then
				self:ApplyLevels()
			end

			if self.shown then
				local s = 1
				if self.camera ~= nil then
					s = _G.Remap(math.clamp(self.camera:GetDistance(), self.camera.mindist, self.camera.maxdist), self.camera.mindist, self.camera.maxdist, 1, 0)
					s = self.minscale + (self.maxscale - self.minscale) * s * s
				end
				s = s * (3 - self.alpha * 2)
				self.bg:SetScale(s, s, s)
			end

			if self.fade <= 0 and self.fadeto <= 0 then
				self.blind = self.blindto
				self:StopUpdating()
			end
		end
	end
end)

AddClassPostConstruct("cameras/followcamera", function(self)
	self:SetDefault()
	
	self.zoomstep = 4
    self.distancetarget = 30
	self.mindist = 15
	self.maxdist = 45
    self.mindistpitch = 30
    self.maxdistpitch = 60
	
	--self:ZoomOut()
	
	local _Update = self.Update
	function self:Update(...)
		_Update(self, ...)
		
		self.mindist = 15
		self.maxdist = 45
		self.zoomstep = 4
		self.mindistpitch = 30
		self.maxdistpitch = 60
		
		if self.distancetarget > 45 then
			self.distancetarget = 45
		elseif self.distancetarget < 15 then
			self.distancetarget = 15
		end
	end
end)